# Assessing

This is the last phase in the lifecycle of a Cognition Actor (CA) before it cycles back to predicting.

Assessing covers doing retrospectives, making adjustments and executing life events.

## Abandon intent if

* it is no longer relevant (the experience to be impacted is gone)
* it is stalled (not executing/executed for N timeframes)
* then drop any plan for it and let umwelt know the intent is abandoned

## Abandon a directive if

* it is no longer relevant or it is stalled
* then drop any plan for it and let the parents know that the directive cannot be executed

## Abandon a plan if

* it is stalled

## Score plans

* over all timeframes, check if goal states went from executed to achieved (have targeted experience impacts been realized?)
* if achieved, score associated executed plans
* the closer in time to goal achievement, the higher the (correlation) score

## Evaluate causal theory

* if none and there's enough history (timeframe count > N), request one from the Apperception Engine
* if too many prediction errors from applying the current causal theory, request a new one (hold on to the old ones)

## Diffuse wellbeing

* broadcast wellbeing status (parents and umwelt are listeners)
* decide how much wellbeing to transfer to which parents and umwelt CAs
  * from reviewing wellbeing status events received
  * and own wellbeing reserves + depletion rates
* send messages transfering wellbeing to needy parents and/or umwelt CAs
  * clear received wellbeing status events

## Trigger life event

* ask SOM to trigger the next life event: apoptosis, replication, division or none
* wait for the SOM to realize it, unless none
  * apoptosis distributes fullness to parents and umwelt
  * replication/division divides fullness equally, integrity is copied, engagement starts full for new CAs
