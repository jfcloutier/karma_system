# Beliefs

## About beliefs

The mind of an agent is an evolving hierarchy of cognition actors (CA). Each CA is a separate process always trying to make sense of what it observes in order to cause the agent to act in ways that are hopefully beneficial.

A CA, by definition, observes its umwelt (via predictions and prediction errors). The umwelt is composed of one-level-down CAs. The CAs and their umwelts form a hierarchy.

Observations in a given timeframe are considered synchronous, as are the beliefs derived in the timeframe.

A CA gets *concrete* beliefs from its causal theory (abduced properties and relations), from sensing properties of its environment (if it is a sensor CA), and from having executed policies/actions.

A CA with an umwelt synthesizes *abstract* beliefs from noticing quantities (counts and comparisons), trends, startings and endings in the beliefs held in its umwelt's CAs.

The CA makes its own beliefs available for observation by its "parent" CAs. And so on, up an abstraction hierarchy of beliefs about beliefs about beliefs etc.

Each CA decides how to act on the basis of its beliefs plus how it felt when deriving them. So beliefs are central to agency.

A CA obfuscates the derivation of its abstract beliefs for observation by by parent CAs,
i.e. the observed beliefs leading to an abstract belief are opaque to the observer of the abstract belief (information hiding).

## Concrete beliefs

The concrete beliefs (not derived from other beliefs) are properties detected by the sensor CAs (e.g. `distance(obstacle, 10)`),
abduced from generating the CA's causal theory (e.g. `property123(object456, true)`, `relation123(object123, object456)`),
and properties from executing simple actions (e.g. `done(motor1, reverse_spin)`) or policies (e.g. `done(CA, Policy)`).

## Abstract beliefs

There are six kinds of abstract beliefs: **started**, **ended**, **count**, **more_of** and **trend**.

Each abstract belief is expressed as a `property` (linking an object and a value) or as a `relation` (linking two objects).

A property is expressed as `Property(Object, Value)` where

* `Property` is a property name
* `Object` is the unique name of an observed belief what's starting, trending, ending, or counted
  * the identity (derivation) of the named object is known only to the CA that named it
  * note that objects are not physical "things"; they are observed beliefs.
* `Value` is a literal belonging to the property's domain (e.g. blue, up, true, 4, etc.)

A relation is expressed as  `Relation(Object, Object)`, where

* `Relation` is a relation name
* Each `Object` is the unique name of an observed `count` belief

### count

> The belief that something can be counted in the current timeframe.

e.g. this action was done twice

* What
  * A property
* Observed as `count(Object, Value)` where
  * `Object` is a unique name possibly created from
    * `Direction(RelationName, InternalObject)` - how many objects connect to/from a given object via a given relation
    * `properties(PropertyName, Value)` - how many objects are known to possess a given property value
  * `Direction` is `to` or `from`
  * `Value` is an enumerated value

### more_of

> The belief that there has been more of something than of something else in the current timeframe.

e.g. there have been more attempts to achieve this goal than attempts to achieve this other goal

* What
  * A relation
* Observed as `more(Object1, Object2)` where
  * `Object1`, `Object2` are unique names created from `count(InternalObject, Value)`

### started

> The belief that something observed in the current timeframe is not part of a trend

e.g. increase in luminance was first observed 3 ticks ago

* What
  * A property
* Observed as `started(Object, Value)` where
  * `Object` is a unique name created from an observed belief
  * `Value` is the number of frames that passed since first observed

### trend

> The belief that the values of a property of an object are trending up or down, as observed over timeframes leading to, and including, the current timeframe.

e.g. luminance is increasing

* What
  * A property
* Observed as `trend(Object, Value)` where
  * `Object` is a unique name created from `properties(PropertyName, InternalObject)`
  * `Value` is `up` or `down`

## ended

> The belief that something is no longer observed in the current timeframe

e.g. increase in luminance ended suddenly

* What
  * A property
* Observed as `ended(Object, Value)` where
  * `Object` is a unique name created from an observed belief
  * `Value` is the number of frames that passed since the observed belief ended

## About naming of objects in beliefs

Names of objects are generated in such as way as to be unique to the semantics of an object.
Objects with the same structure and content will have the same name across CAs.
