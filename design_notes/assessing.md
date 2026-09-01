# Assessing

This is the last phase in the lifecycle of a Cognition Actor (CA) before it cycles back to predicting.

Assessing covers doing retrospectives, making adjustments and executing life events.

## Assessments

When doing the assessment phase of its lifecycle, a CA

* may abandon its current intent (current self-assigned goal)
* may abandon plans it formulated to achieve goals
* determine which executed goals, if any, are now achieved
* give an "efficacy" score to plans which goals were achieved
* decide whether to get an initial or replacement causal theory
* decides how much of its wellbeing to diffuse to its entourage (umwelt and parents)
* asks the SOM for a possible next life event

### Abandon the current intent if

* it is no longer relevant (the experience to be impacted is gone)
* it is stalled (not executed for N timeframes)
* then drop any plan for it and let umwelt know the intent is abandoned

### Abandon a plan if

* it is stalled (it is not yet executed and too many timeframes passed since it was built)

### Assess goal achievement

* for each executed goal, assess whether it was achieved

### Score plans

* for each goals just achieved, score associated executed and remembered plans (affordances)
* the closer in time plan execution is to goal achievement, the higher the (correlation) score
* the more recently used a plan, the higher the score

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

* ask SOM to trigger the next life event: apoptosis (self termination), replication, division or none
* wait for the SOM to realize it, unless none
  * apoptosis distributes fullness to parents and umwelt equally
  * replication/division divides fullness equally, integrity is copied, engagement starts full for new CAs

## Evaluating goal achievement

A goal's target is a property/relation to be experienced (or no longer experienced) because of the execution of a plan.

An experience is a property or relation synthesized from observations (the evidence for the experience).
An object of experience (orgin, and value if a relation) keeps that evidence as a list of observation IDs.
This list is known only to the experiencing CA.

The types of properties/relations a CA experiences (and also observes as experiences of its umwelt) are:

* activation(Object, Value) - a property - the object is a goal (identified by its target and impact) and the value is the current status of the activation (`relevant`, `not_relevant`, `planned`, `failed`, `executed`)
* count(Object, Value) - a property - the value is 1, 2, 3 or many (initially > 1) - the number of observations making up the Object
* more(Object1, Object2) - a relation - the set of observations (Object1) is larger than another (Object2)
* trend(Object, Value)- a property - the value is `up` or `down` or `steady` (characterization of the change in value between prior and current related observations)

A CA intends to or is directed to persist, terminate or create a `count`, `more` or `trend` experience. Activation experiences capture progress toward such goals; predicting their value drives action.

A goal for the CA is achieved if its targeted property/relation is realized as an experience of the CA that is either made present or absent.

It is realized if the value of the current experience is the one targeted and the observation(s) in a targeted experience match the observation(s) in a current experience.

Depending on the type of impact sought, there is a match between the targeted experience and a current experience if one represents a subset of the observations the other represents, or if they represent the same set of observations.

Specifically, a goal is achieved according to these rules:

* If the goal is to persist an experience, the goal is achieved if a current experience has the exact same origin object (with same evidence), kind and value as the goal's target
* If the goal is to terminate an experience, the goal is achieved if there is no current experience with the exact same origin object, kind and value as the goal's target
* If the goal is to create an experience, the goal is achieved if there is a current experience of the same kind and with a value and origin object matching the goal's target
  * values that are not objects match if and only if they are the same
  * how objects as origins or values match depend on the kind of experience (targeted and actual)
    * a "create" goal is either instantiated direcly from a current experience (to impact it) or from the analysis of a causal theory
      * currently, only from a `trend` experience can a "create" goal be directly instantiated from it in order to impact it
      * the goal will be to change the value of a current, numerically-valued observation (a numerically-valued experience in the umwelt), to persist/terminate the trend's current value (based on current vs prior observation)
      * the numerically-valued kinds of experiences included the synthetic `count` experience and sensor experiences such as distance and luminance
      * how a current experience is determined to achieve a "create" goal depends on its kind
        * For example, `count` - a different count is to be realized from the one previously experienced
          * the target's origin object will contain either too many or too few evidential observations compared to the targeted value (it was created from a count experience with a larger or smaller value)
          * if the evidence is undercounted in the target, the sought  `count` experience must have a strict superset of this evidence (in its origin object) - its cardinality gives the experienced count
          * if the evidence is overcounted in the target, the sought `count` experience must have a strict subset of this evidence (etc.)
