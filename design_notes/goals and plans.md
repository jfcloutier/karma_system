# Goals and plans of cognition actors (CAs)

## Definitions

A **goal** is a relation/property a CA aims to impact in a certain way with some priority.

An *intent* is a self-assigned goal (assigned by a CA to itself).

A *directive* is a delegated goal (delegated by a CA to its umwelt CAs).

A **plan** is a set of directives designed by a CA to achieve a goal.

An *affordance* is a plan with an effectiveness score justifying its reuse.

## Data structures

``` prolog
goal{id: ID, target: Target, impact: Impact, priority: Priority, status: Status, plan: Plan | tbd}
```

The plan of a goal is `tbd` when it is delegated to the umwelt.

> Target: target{origin: Origin, kind: Kind, value: Value} - property or relation
>
> Impact :: create | persist | terminate
>
> Status :: none | pending | can_actuate | cannot_actuate | getting_ready | ready | abandoned | executed | achieved | failed
>
> Priority :: 0.0..1.0

Statuses:

* none - not looked at yet
* pending - determining if there is a plan
* can_actuate - there could be a plan for achieving the goal (parent CA was advised)
* cannot_actuate - there is no plan for achieving the goal (parent CA was advised)
* getting_ready - working on a plan
* ready - there is plan to achieve this goal
* abandoned - the CA can no longer actuate or execute (parent CA and umwelt CAs were advised)
* executed - the plan for this goal was executed
* achieved - the goal was achieved after execution of the plan
* failed - the goal was not achieved after execution of the plan

The goal is an intent if it does not appear as directive in any plan received from parent CAs.

``` prolog
plan{id: ID, directives: [Goal, ...], source: Source, status: Status, score: Score}
```

> Source :: self or CA_ID
>
> Status :: none | acknowleged | ready | abandoned | executed
>
> Score: 0.0..1.0 | none

There is at most 1 `goal` in a CA state and per remembered timeframe - the current/then goal.

There can be many `plans_in` in a CA state - plans delegated by parent CAs - but at most 1 `plan` per state or timeframe - the current/then plan attempted.

A CA is in control of the execution of a plan if it is built from an intent, as opposed to a directive.

## Responsibilities per phase

How dedicated phases of a CA's lifecycle affect goals and plans:

### Plan

Before work:

* For each received plan
  * For each directive in a received plan
    * If the directive status is `none`
      * 

Work:

* Select the most important goal among candidates (priority is skewed by weight).
  * In decreasing order by weight:
    * The current `activated` goal if any (maintain focus)
    * Follow-up goals (`activated` directives from the same plan as the current `achieved` goal - for continuity)
    * Other `activated` directives (from any received plan)
    * Intents (goals from threshold-crossing experiences to impact)
* If the selected goal replaces the current goal
  * If the current goal was not `achieved`,
    * Send abandoned_goal(goal=GoalID) to parentCA if a directive
    * Send abandoned_plan(plan=PlanID) to umwelt
    * Mark the goal and plan as `abandoned` (it is being replaced and has neither succeeded not failed)
* If none is selected, the goal is `none`

* If a plan is already `pending` for the selected goal, do nothing
* Else reuse/build a plan to realize the selected goal
  * Assemble a list of directives
  * Emit the plan to the umwelt
  * Mark the goal and plan as `pending`
  
### Act

Work:

* If all directives of the current plan can be actuated by the umwelt
  * If the plan is for a directive,
    * message the parent CA that the CA `can_actuate` the directive
  * If the plan is for an intent, publish the `execute` event for the plan
    * mark the intent goal and plan as `executed`

### Assess

* Check the status of the current goal
  * If the current goal was achieved
    * Mark both goal and plan as `achieved`
    * Update the score of the plan
  * Else if the current goal is stale (too old)
    * Cancel the goal and its associated plan
      * Mark the goal and plan as `failed`
      * If the goal was a directive, message the parentCA with abandoned_goal(goal=goalId)
      * Send event to umwelt abandoned_plan(plan=planId)


## SECOND THOUGHTS

At any time, a CA
 * receives messages
   * from parent
     * to_do (add a plan to the to-do's - a plan is an all-or-none list of goals to achieve)
     * get_ready (asked to find a plan for a directive in a to-do plan)
     * execute (execute the ready plan)
     * abandon (remove a plan from the to_do's)
   * from umwelt
     * can_actuate (could find on a plan for a directive)
     * cannot_actuate (would not be able to a find a plan for a directive)
     * ready (umwelt CA has a plan it can execute to achieve a directive)
     * not_ready (no plan found for a directive)
     * executed (the ready plan was successfully executed)
     * execution_failed (the ready plan failed to be executed)

At the act phase, until the deadline, a CA works to

* Generate a more urgent intent if no intent is progressing toward executed
* Advance toward executed, as priority dictates, the statuses of
  * directives in plans to-do
  * its own intent
  
At the assess phase, a CA works to

* Determine if its intent is stale
  * If so, it abandons the intent
    * Messaging its umwelt it is abandoning its plan for it, if any
* Determine if success or failure of executed plans
  * Were goals achieved or not?
  * Score executed plans
  
Goal status

* none
* can_actuate (the goal relates to experiences)
* cannot_actuate (the goal does not relate to any experience)
* getting_ready (working on a plan)
* ready (the plan is ready)
* executed (the plan was executed)
* achieved (the goal was achieved)
  
Plan status (implicit)

* pending (determining the readiness of directives)
* ready (all directives are ready)
* not_ready (some directives can not be made ready)
* executed (all directives were successfully executed)
* failed (not all directives were successfully executed)
  
Relevant state properties

* plans_in - [Plan, ...] - As sources of directives
* intent - Goal
* plan - Plan
* goal_states - [GoalState, ...] - states of intent or directives in and out

Data structures

goal{id: ID, target: Target, impact: Impact} - 

* ID is determined by Target and Impact

plan{id: ID, directives: [Goal, ...], , priority: Priority, score: Score, by: CA}

* Score is always none for plans in

goal_state{goal: GoalID, plan: [Goal, ...], status: Status, messages: [Message, ...]}

* Messages are latest first

