# Beliefs

## About beliefs

The mind of an agent is an evolving hierarchy of cognition actors (CA). Each CA is a separate process always trying to make sense of what it observes in order to cause the agent to act in ways that are hopefully beneficial.

A CA, by definition, observes its umwelt (via predictions and prediction errors). The umwelt is composed of one-level-down CAs. The CAs and their umwelts form a hierarchy.

Observations in a given timeframe are considered synchronous, as are the beliefs derived in the timeframe.

A CA derives its beliefs from noticing quantities (counts and comparisons), trends, starts, endings in its umwelt.
What it observes are the (starting, accumulating, trending, ending) beliefs, past and present, of its "child" CAs.
The CA makes its own, more abstract beliefs available for observation by its "parent" CAs.
And so on, up an abstraction hierarchy of beliefs about beliefs about beliefs etc.

Each CA decides how to act on the basis of its beliefs plus how it felt when deriving them. So beliefs are central to agency.

The beliefs of a CA are expressed for observation by obfuscating their derivation, i.e. the observed beliefs leading to a belief are opaque to the observer of the belief but retained by the CA holding the observed belief.

The "bottom" beliefs (not derived from other beliefs) are **sensed** beliefs of the sensor CAs and **count* beliefs of the effector CAs (counting how many actions of a kind were executed).
Sensor and effector CAs sit at the bottom of the hierarchy of CAs and interface with the body's sensors and effectors.
A sensor CA simply observes the value of its attached sensor and translates it into a belief.
An effector CA simply tells the body to prepare to actuate an effector and translates execution into a belief.

There are six kinds of beliefs: **imagined**, **sensed**, **started**, **count**, **more**, **trend** and **ended**.

Each belief is expressed as a `property` (linking an object and a value) or as a `relation` (linking two objects).

A property is expressed as `Property(Object, Value)` where

* `Property` is a property name
* `Value` is a literal belonging to the property's domain (e.g. blue, up, true, 4, etc.)
* `Object` is the unique name of what's starting, trending, ending, counted, more of, or sensed
  * e.g. self,  reverse_spin, ahsd34ahsdjh
  * the identity (derivation) of the named object is known only to the CA that named it
  * note that objects are not necessarily physical "things"; they are mostly observed beliefs.

A relation is expressed as  `Relation(Object1, Object2)`, where

* `Relation` is a relation name
* others as above

## Imagined

> Something unobserved needed to formulate a causal theory.

Imagined beliefs are conjured up properties or relations to posit occulted observations needed to causally explain direct observations.

* What
  * A relation `Relation(Object1, Object2)` or property `Property(Object, Value)`
* Observed as-is (i.e. unobfuscated)

## Count

> The belief that something can be counted in the current timeframe.

e.g. this action was executed twice

* What
  * A property
* Observed as `count(Object, Value)` where
  * `Object` is a unique name possibly created from
    * `Direction(RelationName, InternalObject)` - how many objects connect to/from a given object via a given relation
    * `properties(PropertyName, Value)` - how many objects are known to possess a given property value
    * a self-referential object (e.g. an effector CA action)
  * `Direction` is `to` or `from`
  * `Value` is an enumerated value

## More

> The belief that there has been more of something than of something else in the current timeframe.

e.g. there have been more attempts to achieve this goal than attempts to achieve this other goal

* What
  * A relation
* Observed as `more(Object1, Object2)` where
  * `Object1`, `Object2` are unique names created from `count(InternalObject, Value)`

## Started

> The belief that something observed in the current timeframe is not part of a trend

e.g. increase in luminance was first observed 3 ticks ago

* What
  * A property
* Observed as `started(Object, Value)` where
  * `Object` is a unique name created from an observed belief
  * `Value` is the number of frames that passed since first observed

## Trending

> The belief that the values of a property of an object are trending up or down, as observed over timeframes leading to, and including, the current timeframe.

e.g. luminance is increasing

* What
  * A property
* Observed as `trending(Object, Value)` where
  * `Object` is a unique name created from `properties(PropertyName, InternalObject)`
  * `Value` is `up` or `down`

## Ended

> The belief that something is no longer observed in the current timeframe

e.g. increase in luminance ended suddenly

* What
  * A property
* Observed as `ended(Object, Value)` where
  * `Object` is a unique name created from an observed belief
  * `Value` is the number of frames that passed since the observed belief ended

## Sensed

> The **fact** that the CA made a sensor reading.

e.g. distance to obstacle is 10cm

* What
  * A property
* Observed as `sensed(Sensor, Value)` where
  * `Sensor` is the unique name of a sensor
  * `Value` is a sensor reading

## About naming of objects in beliefs

Names of objects are generated in such as way as to be unique to the semantics of an object.
Objects with the same structure and content will have the same name across CAs.
