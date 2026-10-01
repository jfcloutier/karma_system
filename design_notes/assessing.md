# Assessing

This is the last phase in the lifecycle of a Cognition Actor (CA) before it cycles back to the begin phase of its lifecycle.

Assessing covers doing retrospectives, making adjustments and executing life events.

## Assessments

When doing the assessment phase of its lifecycle, a CA

* may abandon its current intent (current self-assigned goal) if it is stale or stalled
* may abandon plans in progress if they are stale or stalled
* give/update a score to affordances (remembered executed plans) to reflect the likelihood of having caused goals to be achieved
* forget affordances if they are not useful enough
* decide whether to get an initial or replacement causal theory
* decides how much of its wellbeing to diffuse to its entourage (umwelt and parents)
* asks the SOM for a possible next life event (should the CA remove itself from the SOM, replicate, divide, or simply go on)

### Abandoning the current intent

Abandon the current intent if:

* it is no longer relevant (the experience to be impacted is gone)
* it is stalled (not executed for N timeframes)

If abandonned, drop any plan for it

### Abandoning a plan

Abandon a plan if it is stalled (it is not yet executed and too many timeframes passed since it was built)

### Evaluating affordances

For each affodance:

* if not yet scored, assess whether its goal was achieved
* if so, score it
  * the closer in time plan execution is to goal achievement, the higher the (correlation) score
  * if there is an older affordance with the same plan, drop the older affordance

If a CA reuses an affordance and the remembered plan is executed, it becomes a separate affordance without a score.

### Evaluating a causal theory

If a CA does not have one yet and if there's enough history (timeframe count > N), request one from the Apperception Engine.

If too many prediction errors are caused from applying the current causal theory, request a new one.

### Diffusing wellbeing

When diffusing wellbeing:

* broadcast wellbeing status (parents and umwelt are listeners)
* decide how much wellbeing to transfer to which parents and umwelt CAs
  * from reviewing wellbeing status events received
  * and own wellbeing reserves + depletion rates
* send messages transfering wellbeing to needy parents and/or umwelt CAs
  * clear received wellbeing status events

### Triggering life event

Ask SOM to trigger the next life event: apoptosis (self termination), replication, division or none

If there's a life event, wait for the SOM to realize it.

Apoptosis distributes fullness to parents and umwelt equally.

Replication/division divides fullness equally, integrity is copied, engagement starts full for new CAs.

## Detecting goal achievement

A goal's target is an experience (specified as its property or relation) from a current or past timeframe to be persisted or terminated in a future timeframe.
A goal is achieved when the desired impact on the targeted experience is realized by the appearance or disappearance of a matching experience.

If the desired impact is to persist or create an experience, then it is realized when an experience is examined in the current timeframe that matches the goal's target (the property or relation of the targeted experience).
If the desired impact is to terminate an experience, then it is realized when no experience is examined in the current timeframe that matches the goal's target.

An examined experience matches a goal's target experience if

* the experience and the goal's target experience are defined by the same kind of property/relation (e.g. both are `count`, `trend`, `distance` etc. experiences),
* the origins of each experienced property/relation match, i.e. what the targeted and examined experiences are about compatible objects
* both property/relation values match (e.g. 14 matches 14, `up` matches `up`, a set of counted observations matches another set. etc.)

The matching rules on origins and values (targeted vs examined) are constrained by the kind of experience:

* Values, if atomic, must be equal (a property's value is atomic whereas a relation's value is an object)
* For `count` experiences:
  * A `count` experience groups observations that have something in common and counts them (it is a property with a number as its value)
    * The group of observations form the origin object of the experience (what the `count` is about)
    * e.g. "two sensors give the same distance"
  * To match, the counted observations must be the same in the targeted and examined experiences (they must have the same origin object)
* For `more` experiences:
  * A `more` experience is a relation between two numerically-valued observations (remember that observations are experiences noted in an umwelt)
    * The origin and value of a `more` experience each represent an observation, with the first observation having a value greater than the second
  * To match, both origin objects (in the targeted vs examined experiences) must be *germane*, and both value objects must also be germane
    * The targeted `more` experience is recognized in the the examined `more` experience
    * Two objects, each representing a numerically-valued observation, are germane if the observations whose values are compared are themselves compatible
      * There are two possible types of numerically-valued observations evidencing a `more` experience, observations of sensory experiences and of `count` experiences
      * Observations of sensory experiences with numerical values (e.g. the distance measured by the front IR sensor) are compatible if they are of the same kind (i.e. same sense, e.g. distance)
      * Observations of `count` experiences (e.g. the number of up trends) are compatible if the counted set of observations is the same as, or is an expansion of, the other
        * i.e. either set of counted observations has shrunk, grown or remained the same
  * For `trend` experiences:
    * A `trend` describes how the value of an observation changes, or not, over time (from timeframe to timeframe)
      * A trend experience has an atomic value of `up`, `down` or `steady`
      * e.g. "the distance read by the front IR sensor is trending down", some `count` remains the same, etc.
    * For a targeted and examined `trend` experiences to match (after we matched their atomic values, e.g. `up` = `up`),
      * the observations evidencing the examined `trend` experience (and forming its origin object) must extend the observations evidencing the targeted `trend` experience
        * i.e. the evidence for the examined trend experience adds observations to the evidence for the targeted trend such that it keeps the trend value `up`, `down` or `steady`
