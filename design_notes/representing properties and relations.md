# Representing properties and relations

Experiences, Predictions, Prediction Errors, Predictables and Observations represent different perspectives held by CAs about properties/relations.

* Observations: The experienced properties/relations a CA perceives of its umwelt CAs
* Predictions: The next observations a CA anticipates
* Prediction errors: Corrections a CA receives from its umwelt about the values of predictions it made
* Predictables: Specifications of what predictions a CA can respond to
* Experiences:  Properties/relations abstracting the CA's past and current observations

Properties/relations are represented as Origin ---Kind--> Value. A relation is between two objects (its origin and its value). A property is between one object (its origin) and an atomic value.

* The origin of a property or relation is an object
* The kind of a property/relation is an atomic name
* The value of a relation is an object
* The value of a property is a number or atom from a domain defined by the property's kind

Observations, Experiences, Predictions and Prediction Errors add meta-data such as `confidence`.

## Kinds of properties/relations

Sensors and effectors name their sense and action properties respectively. The causal theory of a CA can invent properties and relations that it also names. A CA creates properties and relations of three possible pre-defined kinds when it synthesizes experiences by abstracting observations.

* (sense name) - only when the origin is a sensor, e.g. `distance`, `color`, `contact`, `state` etc.
* (action name) - only when the origin is an effector, e.g. `spin`, `reverse_spin`
* (latent property/relation name) - when the property/relation is abduced and named by a causal theory
* (synthesis name) - names of abstractions, namely `count`, `more` or `trend`

## Objects in properties/relations

In properties, the origin is always an object but never the value. In relations, both origin and values are objects.

Sensor and effector objects are a priori and permanent objects. Latent and synthetic objects are created by CAs as part of their sense making efforts.

* (sensor) -> object{type: sensor, id: (sensor name)}
* (effector) -> object{type: effector, id: (effector name)}
* (latent object) -> object{type:(latent type), id:(unique atom)} - when the object is abduced by a causal theory
* (synthetic object) -> object{type:synthetic, id:(unique atom)} - the id references a list of observations in time frames past and current; it is known only to the CA that synthesized the object

## Values of properties and relations

The values of relations are objects and the values of properties are numbers, labels, true/false, etc.

A property's value belongs to the domain defined by the kind of property.

### Values of sense properties

A sensor (or motor) provides the domain of values it can report upon sensing. For examples:

`color`: One of `black`, `white`, `brown`, `yellow`, `green`, `red`, or `blue`
`contact`: Either `pressed` or `released`
`distance`: 0 to 250 (cm)
(motor) `state`: One of `running`, `ramping`, `holding`, or `overloaded`

### Values of effector properties

The values of action properties of effectors (e.g. `spin`) are either `true` or `false`, to designate whether the action was taken or not.

### Values of synthetic properties and relations

A `trend` property (on a set of past and current observations) can have value `up`, `down`, `same` or `ended`.

A `count` property (on a set of current observations) is either `1`, `2`, `3` or `many` because a CA can not count very far and has no notion of zero (this is to mimic the limited counting abilities of simple living beings).

A `more` relation (between sets of current observations - both represented as synthetic objects) indicates that there is more of one group of related observations than of another.

## Representations

### Experience

* (property or relation)
* confidence: 0.0..1.0
* by: (ca)

### Observation

* (property or relation)
* confidence: 0.0..1.0
* by: (ca)
* of: [(unmwelt_ca), ...]

### Predictable

* origin: (object)
* kind: (kind)
* domain: (domain) - boolean, [red, green,...], etc.
* by: (ca)

### Prediction

* (property or relation)
* confidence: 0.0..1.0
* by: (ca)
* for: [(unmwelt_ca), ...]

### Prediction error

* prediction: (prediction)
* actual_value: (value)
* confidence: 0.0..1.0
* by: (ca)
