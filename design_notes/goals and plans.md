# Goals and plans of cognition actors (CAs)

## Definitions

A **goal** is a relation/property of a CA the CA is to impact in a certain way with some priority.
A **plan** is a set of directives designed by a CA to achieve a goal.

An *intent* is a self-assigned goal (assigned by a CA to itself).
A *directive* is a delegated goal (delegated by a CA to its umwelt CAs).
An *affordance* is a plan with an effectiveness score justifying its reuse.

## Data structures

goal{id: ID, target: Target, impact: Impact, priority: Priority, status: Status, of: CA}

    Target: target{origin: Origin, kind: Kind, value: Value} - property or relation
    Impact :: create | persist | terminate
    Status :: none | pending | executed | achieved | failed
    Priority :: 0.0..1.0

plan{id: ID, for_goal: GoalId, directives: [Goal, ...], source: Source, status: Status, score: Score, of: CA}

    Source :: self or CA_ID
    Status :: none | pending | executed | achieved | failed
    Score: 0.0..1.0 | none
    
There is at most 1 `goal` in a CA state and per remembered timeframe - the current/then goal.
There can be many `plans_in` in a CA state - plans delegated by parent CAs - but at most 1 `plan` - the current/then plan being attempted.

A CA is in control of the execution of a plan if it is built from intent, as opposed to a directive.

## Phases

How dedicated phases of a CA's lifecycle affect goals and plans:

### Plan

Before work:

* Select a goal to accomplish
  * It remains the current goal if it is `pending` (a plan was emitted and is pending execution)
  * Else the candidate goals are:
    * The current not-yet-achieved goal
    * Directives (delegated goals) within received plans
    * Goals from threshold-crossing experiences to impact
    * Pick the most important candidate goal
      * A follow-up goal is more important than another of similar priority (continuity)
        * A follow-up goal is a directive from the same plan as the current `achieved` goal
      * A directive is more important than a self-assigned goal of similar priority
    * If the selected goal replaces the current goal
      * If the current goal was not `achieved`,
        * send abandoned_goal(goal=GoalID) to parentCA if a directive
        * send abandoned_plan(plan=PlanID) to umwelt
      * Clear the goal and plan from the state (it has neither succeeded not failed)
  * If none, the goal is `none`

Work:

* If a plan is already `pending` for the selected goal, do nothing
* Else reuse/build a plan to realize the selected goal
  * Assemble a list of directives
  * Emit the plan to the umwelt
  * Mark the goal and plan as `pending`
  
### Act

Work:

* If all directives of the current plan can be actuated by the umwelt
  * If the plan is for a directive,
    * message the parent CA that the directive can be actuated
  * If the plan is for an intent, publish the execute event for the plan
    * mark the intent goal and plan as `executed`

### Assess

* Check the status of the current goal
  * If the current goal was achieved
    * Mark both goal and plan as `achieved`
    * Update the score of the plan
  * Else if the current goal is stale
    * Cancel the goal and its associated plan
      * Mark the goal and plan as `failed`
      * If the goal was a directive, message the parentCA with abandoned_goal(goal=goalId)
      * Send event to umwelt abandoned_plan(plan=planId)
