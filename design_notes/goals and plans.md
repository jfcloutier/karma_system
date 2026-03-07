# Goals and plans

## Definitions

A **goal** is a relation/property a CA aims to impact in a certain way with some priority.

An *intent* is a self-assigned goal (assigned by a CA to itself).

A *directive* is a delegated goal (delegated by a CA to its umwelt CAs).

A **plan** is a set of directives designed by a CA to achieve a goal.

An *affordance* is a plan with an effectiveness score justifying its reuse.

## Between and during phases

During any phase, a CA

* receives messages
  * from parent CAs
    * to_do (add a plan to the to-do's - a plan is an all-or-none list of goals to achieve)
    * get_ready (asked to find a plan for a directive in a to-do plan sent out)
    * execute (execute the ready plan)
    * abandon (remove a plan from the to_do's)
  * from umwelt CAs
    * can_actuate (could find on a plan for a directive)
    * cannot_actuate (can't possibly find a plan for a directive)
    * ready (umwelt CA has a plan it can execute to achieve a directive)
    * not_ready (no plan can be found for a directive)
    * executed (the ready plan was successfully executed)
    * execution_failed (the ready plan failed to be executed)

At the `act` phase, a CA works to

* Generate a more urgent intent if no intent is progressing toward executed
* Advance, as priority dictates, the statuses of
  * directives in plans to-do (toward executed)
  * its own intent
  
At the `assess` phase, a CA works to

* Determine if its intent is stale
  * If so, it abandons the intent
    * It messages its umwelt that it is abandoning its plan for it, if any
* Determine the success or failure of executed plans
  * Were goals achieved or not?
  * Score executed plans built by the CA

## Data
  
### Goal status

* none
* can_actuate (the goal relates to experiences)
* cannot_actuate (the goal does not relate to any experience)
* getting_ready (working on a plan)
* ready (the plan is ready)
* executed (the plan was executed)
* achieved (the goal was achieved)
  
### Plan status (implicit)

* pending (determining the readiness of directives)
* ready (all directives are ready to have plans executed)
* not_ready (some directives can not be made ready)
* executed (all directives were successfully executed)
* failed (not all directives were successfully executed)
  
### Relevant state properties

* plans_in - [Plan, ...] - As sources of directives
* intent - Goal
* plan - Plan - for the intent
* goal_states - [GoalState, ...] - states of intent or directives in and out

### Data structures

`goal{id: ID, target: Target, impact: Impact}`

> ID is determined by Target and Impact
>
> Target: target{origin: Origin, kind: Kind, value: Value} - property or relation
>
> Impact :: create | persist | terminate
>

`plan{id: ID, directives: [Goal, ...], , priority: Priority, score: Score, by: CA}`

> Priority :: 0.0..1.0
>
> Score: 0.0..1.0 | none - Score is always none for plans received

`goal_state{goal: GoalID, plan: [Goal, ...], status: Status, messages: [Message, ...]}`

> Source :: self or CA_ID
>
> Status :: none | can_actuate | cannot_actuate | getting_ready | ready | executed | achieved
>
> Messages - message received about the goal, latest first
