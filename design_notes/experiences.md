# Experiences

## About experiences

The mind of an agent is an evolving hierarchy of cognition actors (CA). Each CA is a separate process always trying to make sense of what it observes in order to cause the agent to act in ways that are hopefully beneficial.

A CA, by definition, observes its umwelt (via predictions and prediction errors). Its umwelt is composed of one-level-down CAs. The CAs and their umwelts form a hierarchy.
At the bottom of the hierachy sit sensor CAs, with body sensors as their umwelt, and effector CAs, with body effectors as their umwelt.

The agent's umwelt is the world as perceived by the integration of the CAs' umwelts.

Observations in a given timeframe are considered synchronous, as are the experiences derived in the timeframe.

A CA gets *concrete* experiences from directly sensing properties of its environment (if it is a sensor CA), from acting in/on the environment, and from its causal theory in the form of the properties and relations imagined in order to unify the theory.

A CA synthesizes *abstract* experiences from observations of its umwelt. It notices quantities (counts and comparisons), coincidences and trends in the observed experiences of its umwelt.

The CA makes its own experiences available for observation by its "parent" CAs. And so on, up an abstraction hierarchy of experiences about experiences about experiences etc.

Each CA decides how to act on the basis of its experiences plus how it felt when deriving them. So experiences are central to agency.

A CA is constrained by wellbeing considerations in the quantity and nature of experiences it holds; believing and acting on experiences is needed to maintain engagement wellbeing, but it is also a draw on fullness, which is a shared and limited resource.

A CA hides information. It keeps to itself how it derived its abstract experiences offered for observation by parent CAs; the observed experiences leading to an abstract experience are opaque to the observer of that abstract experience.

## Representing experiences

An experience, whether concrete or abstract, is represented, depending on its type, either as a property or as a relation.

A property is expressed as `Property(Object, Value)` where

* `Property` is a property name
* `Object` is the unique name of an observed experience what's starting, trending, ending, or counted
  * the identity (derivation) of the named object is known only to the CA that named it
  * note that objects are not physical "things"; they are observed experiences.
* `Value` is a literal belonging to the property's domain (e.g. blue, up, true, 4, etc.)

A relation is expressed as  `Relation(Object, Object)`, where

* `Relation` is a relation name
* `Object` is a name of an observed experience (note that an object can no relate to itsef)

Note that the object of a CA's experience is not a physical object but an observed experience in the CA's umwelt.

## Concrete experiences

The concrete experiences (experiences not derived from other experiences) are

* properties detected by the sensor CAs
  * `Sense(Sensor, Value)`, e.g. `distance(obstacle, 10)`
* properties from actuations
  * `Action(Effector, Boolean)`, e.g. `reverse_spin(motor1, true)` - an actuation is true once executed and false once the reverse actuation is executed
* properties or relations imagined/abduced when generating a unified causal theory for the CA
  * e.g. `property123(object456, true)`, `relation123(object123, object456)`

## Abstract experiences

Abstract experiences are composed by a CA of *multiple* observations by the CA (of experiences in its umwelt), past and/or present.

There are four kinds of abstract experiences: **count**, **more**, **coincide**, and **trend**.

Each abstract experience is expressed as a `property` (linking an object and a value) or as a `relation` (linking two objects). Remember that objects are made of observed experiences.

### count

> The experience that something can be counted in the current timeframe.

e.g. this motor spun twice, this object coincides with three others, there are two upward trends

* What
  * A property
* Observed as `count(Object, Value)` where
  * `Object` is a unique name possibly created from
    * `Direction(RelationName, InternalObject)` - how many objects connect to/from a given object via a given relation
    * `properties(PropertyName, Value)` - how many objects are known to possess a given property value
  * `Direction` is `to` or `from`
  * `Value` is an enumerated value

### more

> The experience that there has been more of something than of something else in the current timeframe.

e.g. this motor executed more spins than this other motor, the distance reported by a sensor is greater than the distance reported by this other sensor

* What
  * A relation
* Observed as `more(Object1, Object2)` where
  * `Object1`, `Object2` are unique names created from `count(Object, Value)`

### coincide

> The experience that two or more umwelt experiences are consistently co-occuring

e.g. increase in luminance and reduction in distance are observed together

* What
  * A property
* Observed as `coincide(Object, Boolean)` where
  * `Object` names a set of experiences
  * `Boolean` is true if all experiences in the set are currently observed

### trend

> The experience that the ordinal values of a property of an object is trending up or down or not at all, as observed over timeframes leading to, and including, the current timeframe.

e.g. luminance from this sensor is increasing, the number of coincidences with this object is decreasing

* What
  * A property
* Observed as `trend(Object, Value)` where
  * `Object` is a unique name created from `trending(PropertyName, Object)`
  * `Value` is `up` or `down` or `none`

## Elevating experiences

A CA's experience can be "elevated" to also be, as-is, the experience of a parent CA (the parent CA's experience is a "pointer" to the child's experience).

An experience from a child CA can be elevated

* if it is not contradicted by a sibling CA
* the elevated experience is not a component of an abstract experience of the parent CA
  * the CA has "abstracted out" the child's experience

## An experience economy

A CA works to increase engagement by holding useful experiences and by acting on them. However, creating and holding experiences is costly and the CA has limited resources.

A CA will not synthesize all possible abstract experiences it can all at once, only a few to reduce drain on fullness. This relates to attention.

Abstract experiences of no use to parent CAs are eventually dropped, freeing resources for holding other experiences. Elevated experiences are free.

If a parent CA predicts an experience the child CA does not hold (and is possibly not yet in its experiences domain), the child CA will attempt to synthesize it (since it matters), potentially at the expense of another, less useful, experience.

A CA will try not to drop a held experience that is of use to a parent CA (useful because predictions about the experience are received) because doing so reduces the CA's engagement wellbeing.

## Experience domains

The experience domain of a CA is a representation that subsumes all experiences held by the CA.

The experience domain of a CA grows and shrinks with the experiences it holds.

A CA advertises changes to its experience domain so that parent CAs know what they can predict that might not be inferrable from their causal theory.

Experience domains constrain what a parent CA can predict of their umwelt's experiences, and thus constrain what a CA can observe, and thus the signatures of their causal models.

## About naming of objects in experiences

Names of objects are generated in such as way as to be unique to the semantics of an object.
Objects with the same structure and content will have the same name across CAs.
