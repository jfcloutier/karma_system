# Assessing

This is the last phase in the lifecycle of a Cognition Actor (CA) before it cycles back to predicting.

Assessing covers doing retrospectives, making adjustments and executing life events.

## Assessments

When doing the assessment phase of its lifecycle, a CA

* may abandon its current intent (sel-assigned goal)
* may abandon one or more directives (goals received)
* may abandon plans it formulated to achieve a goals
* determine which executed goals, if any, are now achieved
* give an "efficacy" score to plans of achieved goals
* decide whether to get a first/replacement causal theory
* decides how much of its wellbeing to diffuse to its entourage(umwelt and parents)
* asks the SOM for its next life event, if any

### Abandon intent if

* it is no longer relevant (the experience to be impacted is gone)
* it is stalled (not executing/executed for N timeframes)
* then drop any plan for it and let umwelt know the intent is abandoned

### Abandon a directive if

* it is no longer relevant
* then drop any plan for it and let the parents know that the directive status moved/reverted to cannot_seek

### Abandon a plan if

* it is stalled

### Assess goal achievement

* for each executed goal, assess whether it was achieved

### Score plans

* over all timeframes, check if goal states went from executed to achieved (have targeted experience impacts been realized?)
* if achieved, score associated executed plans
* the closer in time to goal achievement, the higher the (correlation) score

### Evaluate causal theory

* if none and there's enough history (timeframe count > N), request one from the Apperception Engine
* if too many prediction errors from applying the current causal theory, request a new one (hold on to the old ones)

### Diffuse wellbeing

* broadcast wellbeing status (parents and umwelt are listeners)
* decide how much wellbeing to transfer to which parents and umwelt CAs
  * from reviewing wellbeing status events received
  * and own wellbeing reserves + depletion rates
* send messages transfering wellbeing to needy parents and/or umwelt CAs
  * clear received wellbeing status events

### Trigger life event

* ask SOM to trigger the next life event: apoptosis, replication, division or none
* wait for the SOM to realize it, unless none
  * apoptosis distributes fullness to parents and umwelt
  * replication/division divides fullness equally, integrity is copied, engagement starts full for new CAs

## Evaluating goal achievement

A goal's target is a property/relation to be experienced.

An object in a property or relation is the opaque synthesis (opaque to other CAs) of one or more observations made by the CA.

The types of properties/relations a CA experiences (and also observes as experiences of its umwelt) are:

* activation(Object, Value) - a property - the value is the number of executions
* count(Object, Value) - a property - the value is 1, 2, 3 or many (initially > 1) - the number of observations "in" the Object
* more(Object1, Object2) - a relation - the set of observations (Object1) is larger than another (Object2)
* unchanged(Object, Value)- a property - the value is 2, 3 or `many` (the number of contiguous, prior timeframes with the same observation)
* trend(Object, Value)- a property - the value is `up` or `down` or `ended` (characterization of the change in value between prior and current related observations)

A goal for the CA is achieved if its targeted property/relation is realized as an experience of the CA.

It is realized if the value of the current experience is the one targeted and the observation(s) in a targeted experience match the observation(s) in a current experience.

Depending on the type of impact sought, there is a match between the targeted experience and a current experience if one represents a subset of the observations the other represents, or if they represent the same set of observations.

Specifically, a goal is achieved according to these rules:

* Given the impact is to persist an experience, the goal is achieved if a current experience has same object, kind and value as the goal's target
* Given the impact is to terminate an experience, the goal is achieved if there is no current experience with same object, kind and value as the goal's target
* Given the impact is to create an experience, the goal is achieved if there is a current experience of the same kind with a value matching the goal's targeted value
  * if the target is a relation, the targeted value (a set of observations) is a strict subset of the experienced value.
