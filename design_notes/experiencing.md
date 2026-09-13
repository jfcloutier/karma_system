# Experiences

## About experiences

The mind of an agent is an evolving hierarchy of cognition actors (CA). Each CA is a separate process always trying to make sense of what it observes in order to cause the agent to act in ways that are hopefully beneficial.

A CA, by definition, observes its umwelt (via predictions and prediction errors). Its umwelt is composed of one-level-down CAs. The CAs and their umwelts form a hierarchy.
At the bottom of the hierachy sit sensor CAs interfacing with body sensors, and effector CAs interfacing with body effectors.

The agent's umwelt is the world as experienced by its collective of CAs.

Observations by a CA in a given timeframe are considered synchronous, as are the experiences derived in the timeframe.

A CA gets *objective* experiences from directly sensing properties of its environment (if it is a sensor CA), from planned goal activations, and from its causal theory in the form of the properties and relations imagined in order to unify the theory. An objective experience is about a singular object: a sensor, a goal, an object imagined by a causal theory.

A CA gets *synthetic* experiences from the synthesis of observed umwelt experiences. Synthesis produces `count`,`more`, and `trend` experiences from observing what the umwelt experiences. A synthetic experience is thus about a set of observations.

The CA makes its own experiences available for observation by its "parent" CAs. And so on, up an abstraction hierarchy of experiences about experiences about experiences etc.

Each CA decides how to act on the basis of its experiences plus how it felt when deriving them. So experiences are central to agency.

A CA is constrained by wellbeing considerations in the quantity and nature of experiences it holds; acquiring experiences and acting on them is needed to maintain wellbeing.

A CA hides information. It keeps to itself how it derived its synthetic experiences when it offers them for observation by parent CAs.

## Representing experiences

An experience, whether objective or synthetic, is represented, depending on its type, either as a property or as a relation.

A property is expressed as `Property(Object, Value)` where

* `Property` is a property name
* `Object` is what the experience is about (a sensor, observations, a goal, an object imagined by a causal theory)
  * an object is described by
    * its type: sensor, observations, goal, imagined
    * its id: respectively, the sensor's or effector's id, a hash of the observations from which the experience was synthesized, the id of a goal, the id of an object imagined by a causal theory.
  * If an experience is synthetic (about and evidenced by multiple observations), only the experiencing CA knowns what these observations are.
* `Value` is a literal belonging to the property's domain (e.g. blue, up, true, 4, etc.)

A relation is expressed as  `Relation(Object, Object)`, where

* `Relation` is a relation name
* `Object` is either the subject or object of a relational experience (note that an object can not relate to itsef)

Note that the object of a CA's experience is not a physical object as we humans understand it but the "aboutness" of the experience.

## Objective experiences

The objective experiences (experiences about singular, identified objects) are

* properties detected by the sensor CAs
  * Sense(Sensor, Reading), e.g. `distance(ir_sensor, 12)` - the distance reported by the infrared sensor is 12
* properties or relations imagined/abduced when generating a unified causal theory for the CA
  * an inferred (as opposed to observed) property or relation e.g. `property123(object456, true)` - an unobserved object with id object456 has unobserved property names property123
* properties from goal activations (leading to and including executions of plans meant to achieve goals)
  * activation(Goal, Status), e.g. `activation(goal_1, executed)` - some plan for achieving the goal with id goal_1 was executed by the CA

### Activation experiences

A CA experiences the activation status of its own goals. Its goals are its own intent and the directives it received from parent CAs predicting their activations as `planned`.

A CA experiences the activation status of its goals from observing the activation status of each directive in the plans it built for these goals.

A goal of the CA has activation status:

* The possible values of goal activation experience are:

  * `failed` - if every directive in the goal's plan is observed as having activation status `failed`
  * else `executed` - if every directive in the goal's plan is observed as having activation status `executed`
  * else `planned` - if every directive in the goal's plan is observed as having activation status `planned` or `executed`
  * else `relevant` - if every directive in the goal's plan is observed as having activation status `relevant`, `planned` or `executed`

## Synthetic experiences

Synthetic experiences combine multiple, compatible observations, past ot present as *evidence* for the experience.

There are 3 kinds of synthetic experiences available to a CA: **count**, **more**, and **trend**.

The evidence for a synthetic experience is a non-empty, maximal set of observations to which the kind applies.
For example if a count of 2 can be enlarged to 3 given the available evidence, then it must be.

### count

> The experience that compatible observations can be counted in the current timeframe.

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
  * `Object` synthesizes trending observations from a continuous past to the present
  * `Value` is `up` or `down` or `steady`

### Updating prior synthetic experiences

* Before work, update prior experiences
  * A prior experience may no longer exist,
  * or a count may take value 1 (counts are initially detected with values > 1)

### Assigning a confidence to a synthetic experience

* Take the minimum confidence in the observed set(s) composing the synthetic object(s) of the experience.
* If a `trend`, boost the minimum confidence with the number of continuous trending observations (the longer the trend, the more confidence in it).

## An experience economy

A CA works to increase engagement by holding useful experiences and by acting on them. However, creating and holding experiences is costly and the CA has limited resources.

A CA will not instantiate all possible synthetic experiences it can all at once, only a few to reduce drain on fullness. This relates to attention.

Synthetic experiences of no use to parent CAs are eventually dropped, freeing resources for holding other experiences.

If a parent CA predicts an experience the child CA does not hold but could, the child CA will attempt to synthesize it since it matters.

A CA will try not to drop a held experience that is relevant to a parent CA (indicated by predictions received about the experience).

## About the naming of objects in experiences

Names of objects are generated in such as way as to be unique to the semantics of an object.
If two objects define the same "aboutness", they will have the same id. If not, they won't.
Thus, objects with the same structure and content will have the same name across all CAs.
