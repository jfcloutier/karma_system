# Assessing

This is the last phase in the lifecycle of a Cognition Actor (CA) before it cycles back to the begin phase of its lifecycle.

Assessing covers doing retrospectives, making adjustments and executing life events.

## Assessments

When doing the assessment phase of its lifecycle, a CA

* may abandon its current intent (current self-assigned goal)
* may abandon plans it formulated to achieve goals
* give/update a score to affordances (executed plans) to reflect the likelihood of having caused goals to be achieved
* decide whether to get an initial or replacement causal theory
* decides how much of its wellbeing to diffuse to its entourage (umwelt and parents)
* asks the SOM for a possible next life event

### Abandon the current intent if

* it is no longer relevant (the experience to be impacted is gone)
* it is stalled (not executed for N timeframes)
* then drop any plan for it and let umwelt know the intent is abandoned

### Abandon a plan if

* it is stalled (it is not yet executed and too many timeframes passed since it was built)

### Score plans

* for affordance (remembered executed plan), assess whether its goal was achieved
* if so, score it
  * the closer in time plan execution is to goal achievement, the higher the (correlation) score
  * the more recently used a plan, the higher the score (it's still working)

### Evaluate causal theory

* if none and there's enough history (timeframe count > N), request one from the Apperception Engine
* if too many prediction errors are caused from applying the current causal theory, request a new one (hold on to the old ones)

### Diffuse wellbeing

* broadcast wellbeing status (parents and umwelt are listeners)
* decide how much wellbeing to transfer to which parents and umwelt CAs
  * from reviewing wellbeing status events received
  * and own wellbeing reserves + depletion rates
* send messages transfering wellbeing to needy parents and/or umwelt CAs
  * clear received wellbeing status events

### Trigger life event

* ask SOM to trigger the next life event: apoptosis (self termination), replication, division or none
* if there's a life event, wait for the SOM to realize it
  * apoptosis distributes fullness to parents and umwelt equally
  * replication/division divides fullness equally, integrity is copied, engagement starts full for new CAs

## Detecting goal achievement

A goal is achieved when the desired impact on the targeted experience is realized by the appearance or disappearance of a matching experience.

If the the desired impact is to persist or create an experience, then it is realized when a experience is held and matches the goal's target.
If the the desired impact is to terminate an experience, then it is realized when no experience is being held that matches the goal's target.

The goal's target is the experience in a current or past timeframe to be persisted or terminated in a future timeframe.

An examined experience matches a goal's target if the experience and the goal's target are of the same kind,
and if both their origin objects and their values match, as constrained by the kind of targeted experience.

Matching rules (targeted vs examined):

* *Atomic* values of the targeted and examined experiences must be the identical to match
* Targeted and examined experiences must be of the same kind (as noted above)
* For `count` experiences:
  * A `count` experience groups observations that have something in common and counts them
  * e.g. two sensors give the same distance
  * To match, the observations (evidencing a count) must be the same in the targeted and examined experiences
* For `more` experiences:
  * A `more` experience relates two numerically-valued observations (short for observations of numerically-valued experiences)
    * The origin and value of a `more` experience each represent an observation, with the first observation having a value greater than the second
  * To match, both origin objects (in the targeted and examined experiences) must be *germane*, and both value objects must also be germane
  * Two objects each representing a numerically-valued observation are germane if the observations are compatible in the context of a `more` experience
  * There are two possible types of numerically-valued observations evidencing a `more` experience
    * observations of sensory experiences with numerical values (e.g. the distance measured by the front IR sensor)
    * observations of `count` experiences (e.g. the number of up trends)
  * Two sensory observations (observations of sensory experiences) are compatible if they are of the same kind (same sense, e.g. distance) and are numerically-valued
  * Two `count` observations are compatible if what one counts is the same as, or is an expansion of, the other (we have more of this than of that)
* For `trend` experiences:
  * A `trend` qualifies how the value of an observed experience changes, or not, over time (from timeframe to timeframe)
    * A trend experience has an atomic value of `up`, `down` or `steady`
    * e.g. the distance read by the front IR sensor is trending down
  * For a targeted and examined `trend` experiences to match (we have already matched their atomic values)
    * the observations evidencing the examined `trend` experience trends must extend the observations evidencing the targeted `trend` experience
