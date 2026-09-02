# Experiences

## About experiences

The mind of an agent is an evolving hierarchy of cognition actors (CA). Each CA is a separate process always trying to make sense of what it observes in order to cause the agent to act in ways that are hopefully beneficial.

A CA, by definition, observes its umwelt (via predictions and prediction errors). Its umwelt is composed of one-level-down CAs. The CAs and their umwelts form a hierarchy.
At the bottom of the hierachy sit sensor CAs interfacing with body sensors, and effector CAs interfacing with body effectors.

The agent's umwelt is the world as experienced by its collective of CAs.

Observations by a CA in a given timeframe are considered synchronous, as are the experiences synthesized/derived in the timeframe.

A CA gets *direct* experiences from directly sensing properties of its environment (if it is a sensor CA), from acting in/on the environment, and from its causal theory in the form of the properties and relations imagined in order to unify the theory.

A CA gets *indirect* experiences from the synthesis or elevation of observations of its umwelt's experiences. Synthesis produces `count`,`more`, and `trend` experiences from observed experiences of its umwelt. It also gets indirect experiences from observaing goal activations in its umwelt.

The CA makes its own experiences available for observation by its "parent" CAs. And so on, up an abstraction hierarchy of experiences about experiences about experiences etc.

Each CA decides how to act on the basis of its experiences plus how it felt when deriving them. So experiences are central to agency.

A CA is constrained by wellbeing considerations in the quantity and nature of experiences it holds; acquiring experiences and acting on them is needed to maintain wellbeing.

A CA hides information. It keeps to itself how it derived its synthetic experiences when it offers them for observation by parent CAs; the observed experiences leading to a synthetic experience are opaque to the observer of that experience.

## Representing experiences

An experience, whether direct or indirect, is represented, depending on its type, either as a property or as a relation.

A property is expressed as `Property(Object, Value)` where

* `Property` is a property name
* `Object` is what the experience is about (a sensor, observations, a goal)
  * an object is described by
    * its type: sensor, observations, goal
    * its id: respectively, the sensor's or effector's id, a hash of the observations from which the experience was synthesized, or the id of a goal.
  * If an experience is synthetic (about and evidenced by multiple observations), only the experiencing CA knowns what these observations are.
* `Value` is a literal belonging to the property's domain (e.g. blue, up, true, 4, etc.)

A relation is expressed as  `Relation(Object, Object)`, where

* `Relation` is a relation name
* `Object` is either the subject or object of a relational experience (note that an object can not relate to itsef)

Note that the object of a CA's experience is not a physical object but the "aboutness" of the experience.

## Direct experiences

The direct experiences (experiences not derived from observed experiences) are

* properties detected by the sensor CAs
  * Sense(Sensor, Reading), e.g. `distance(ir_sensor, 12)` - the distance reported by the infrared sensor is 12
* properties from actuations by the effector CAs
  * actuation(Effector, Action), e.g. `actuation(left_motor, spin)`
* properties from goal activations (leading to and including executions of plans meant to achieve goals)
  * activation(Goal, Status), e.g. `activation(goal_1, executed)` - some plan for achieving the goal with id goal_1 was executed by the CA
* properties or relations imagined/abduced when generating a unified causal theory for the CA
  * an inferred (as opposed to observed) property or relation e.g. `property123(object456, true)` - an unobserved object with id object456 has unobserved property names property123

## Indirect experiences

Indirect experiences are about observed experiences in the CA's umwelt.

Synthetic experiences combine multiple observations, past ot present.

There are 3 kinds of synthetic experiences: **count**, **more**, and **trend**.

See [Synthesizing experiences](../synthesizing_experiences.md)

### count

> The experience that something can be counted in the current timeframe.

e.g. this motor spun twice, there are two upward trends

* What
  * A property
* Predicate `count(Object, Value)` where
  * `Object` synthesizes countable observations
    * Same kind and value - counting objects with same description, or
    * Same origin and kind - counting alternate relations of a kind for one object
  * `Value`  is 1, 2, 3 or `many` (initially > 1)

### more

> The experience that there has been more of something than of something else in the current timeframe.

e.g. this motor executed more spins than this other motor, the distance reported by a sensor is greater than the distance reported by this other sensor

* What
  * A relation
* Predicate `more(Object1, Object2)` where
  * `Object1`, `Object2` synthesizes counted observations (there are more observations synthesized as Object1 than as Object2)

### trend

> The experience that the ordinal values of a property of an object is trending up or down or keeping steady, as observed over timeframes leading to, and including, the current timeframe.

e.g. luminance from this sensor is increasing, the distance is decreasing, the trend in distances is steadily up

* What
  * A property
* Predicate `trend(Object, Value)` where
  * `Object` synthesizes trending observations
  * `Value` is `up` or `down` or `steady`

## Experiencing activations

* A CA experiences an activation
  * **directly**, when it is about its intent
  * **indirectly**, from predicting (and thus observing) the activation status of a directive in a plan it built to achieve a goal

* The possible values of an activation experience are

  * `not_relevant` - the goal (the activation is about) has no meaning - it does not relate to any experience of the CA
  * `relevant` - the goal has meaning
  * `planned` - there's a working plan for the goal
  * `executed` - a plan for the goal was recently executed
  * `failed` - the CA recently failed to build or execute a plan

## An experience economy

A CA works to increase engagement by holding useful experiences and by acting on them. However, creating and holding experiences is costly and the CA has limited resources.

A CA will not instantiate all possible synthetic experiences it can all at once, only a few to reduce drain on fullness. This relates to attention.

Indirect experiences of no use to parent CAs are eventually dropped, freeing resources for holding other experiences.

If a parent CA predicts an experience the child CA does not hold (and is possibly not yet in its experiences domain), the child CA will attempt to synthesize it (since it matters), potentially at the expense of another, less useful, experience.

A CA will try not to drop a held experience that is of use to a parent CA (useful because predictions about the experience are received) because doing so reduces the CA's engagement wellbeing.

## About naming of objects in experiences

Names of objects are generated in such as way as to be unique to the semantics of an object.
If two objects define the same "aboutness", they will have the same id. If not, they won't.
Thus, objects with the same structure and content will have the same name across all CAs.
