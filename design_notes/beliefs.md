# Beliefs

## About beliefs

The mind of an agent is an evolving hierarchy of cognition actors (CA). Each CA is a separate process always trying to make sense of what it observes in order to cause the agent to act in ways that are hopefully beneficial.

A CA, by definition, observes its umwelt (via predictions and prediction errors). The umwelt is composed of one-level-down CAs. The CAs and their umwelts form a hierarchy.

Observations in a given timeframe are considered synchronous, as are the beliefs derived in the timeframe.

A CA gets *concrete* beliefs from its causal theory (abduced/imagined properties and relations), from sensing properties of its environment (if it is a sensor CA), and from acting in/on the environment.

A CA with an umwelt synthesizes *abstract* beliefs from noticing quantities (counts and comparisons), trends, startings and endings in the beliefs held in its umwelt's CAs.

The CA makes its own beliefs available for observation by its "parent" CAs. And so on, up an abstraction hierarchy of beliefs about beliefs about beliefs etc.

Each CA decides how to act on the basis of its beliefs plus how it felt when deriving them. So beliefs are central to agency.

A CA obfuscates the derivation of its abstract beliefs for observation by by parent CAs,
i.e. the observed beliefs leading to an abstract belief are opaque to the observer of the abstract belief (information hiding).

## Representing beliefs

A belief is represented, depending on its types, as a property or as a relation.

A property is expressed as `Property(Object, Value)` where

* `Property` is a property name
* `Object` is the unique name of an observed belief what's starting, trending, ending, or counted
  * the identity (derivation) of the named object is known only to the CA that named it
  * note that objects are not physical "things"; they are observed beliefs.
* `Value` is a literal belonging to the property's domain (e.g. blue, up, true, 4, etc.)

A relation is expressed as  `Relation(Object, Object)`, where

* `Relation` is a relation name
* Each `Object` is a different name (an object is never related to itself)

## Concrete beliefs

The concrete beliefs (not derived from other beliefs) are

* properties detected by the sensor CAs (e.g. `distance(obstacle, 10)`),
* properties or relations abduced from generating the CA's causal theory (e.g. `property123(object456, true)`, `relation123(object123, object456)`),
* properties from executing simple actions (e.g. `reverse_spin(motor1, true)`).

## Abstract beliefs

Abstract beliefs are composed of *multiple* observations (of child CA beliefs), past and/or present.

There are four kinds of abstract beliefs: **count**, **more_of**, **coincide**, and **trend**.

Each abstract belief is expressed as a `property` (linking an object and a value) or as a `relation` (linking two objects).

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
* Observed as `more_of(Object1, Object2)` where
  * `Object1`, `Object2` are unique names created from `count(Object, Value)`

### coincide

> The belief that two or more umwelt beliefs are observed simultanesouly

e.g. increase in luminance and reduction in distance are both observed

* What
  * A property
* Observed as `coincide(Object, Boolean)` where
  * `Object` names a set of beliefs
  * `Boolean` is true if all beliefs in the set are currently observed

### trend

> The belief that the values of a property of an object are trending up or down or not at all, as observed over timeframes leading to, and including, the current timeframe.

e.g. luminance is increasing

* What
  * A property
* Observed as `trend(Object, Value)` where
  * `Object` is a unique name created from `properties(PropertyName, InternalObject)`
  * `Value` is `up` or `down` or `none`

## Elevating beliefs

A CA's belief can also be its parent's belief.

A belief from a child CA can be elevated to a parent CA

* if it is not contradicted by a sibling CA
* and only while the elevated belief is not a component of an abstract belief of the parent CA
  * the CA has "abstracted out" the child's belief

## A belief economy

A CA works to increase engagement by holding useful beliefs and acting on them. However, creating and holding beliefs is costly and the CA has limited resources.

A CA will not synthesize all possible abstract beliefs it can at once, only a many as fullness allows.

Abstract beliefs of no use to parent CA are eventually dropped, freeing resources for holding other beliefs.

If a parent CA predicts a belief the child CA does not hold, the child CA will attempt to synthesize it (since it matters), possibly at the expense of another, less useful, belief.

A CA will try not to drop a held belief that is of use to a parent CA (predictions in the belief domain are received) because doing so reduces engagement wellbeing

## Belief domains

A CA advertises changes to its belief domain which is a representation of the prediction that are meaningful to it.

The belief domain of a CA grows and shrinks with the beliefs it holds; the domain must always subsume all beliefs held. Belief domains constrain what parent CA can predict of their umwelt's beliefs, and thus constrain what a CA can observe, and thus the signatures of their causal models.

## About naming of objects in beliefs

Names of objects are generated in such as way as to be unique to the semantics of an object.
Objects with the same structure and content will have the same name across CAs.
