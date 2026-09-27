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

A goal is achieved when the desired impact on the targeted experience is realized.

If the the desired impact is to persist or create an experience, then it is realized when a experience is held that matches the goal's target.
If the the desired impact is to terminate an experience, then it is realized when no experience is being held that matches the goal's target.

The goal's target is the experience in a current or past timeframe to be persisted or terminated in a future timeframe.

An experience matches a goal's target if the experience and the goal's target are of the same kind,
and both their origin objects and their values match, as constrained by the kind of target/experience.

Matching rules (is there a current experience that matches the target experience?)

* Atomic values must be equal to match
* Is a `count` experience the one targeted (to persist or terminate)?
  * The count value is the same but are the same observations being counted?
    * target.origin.evidence is the same set as experience.origin.evidence (if not, it's another count)
* Is a `more` experience the one targeted
  * Does the 'more' experience (between numerically-valued observations) compare the same things?
    * the evidence being compared is either
      * a pair of sensory observations (e.g. the front IR sensor distance is greater than the back sonic sensor distance)
      * or a pair of count observations (e.g. the count of up trends is greater than the count of down trends)
  * for sensory evidence
    * are the same sensors being compared on each side of the comparison?
      * target.origin.evidence.origin == experience.origin.evidence.origin
      * target.value.evidence.origin == observation.value.evidence.origin
    * are the same senses of these sensors being compared on each side of the comparison?
      * target.origin.evidence.kind == observation.origin.evidence.kind
      * target.value.evidence.kind == observation.value.evidence.kind
  * for count observations (we are looking for the evidence sets that are counted staying the same, growing or shrinking)
    * observation.origin.evidence is equal to, or a superset of, target.origin.evidence (the more-than, counted evidence is the same or has grown)
    * observation.value.evidence is equal to, or a subset of, target.value.evidence (the less-than, counted evidence is the same or has shrunk)
* Is a `trend` experience the one targeted?
  * TODO
