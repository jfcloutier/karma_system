# Representing properties and relations

Experiences, Predictions, Prediction Errors, Predictables and Observations of CAs are about properties or relations.

They represent different perspectives held by CAs about properties/relations:

* Observations: What a CA perceives of the experiences of its umwelt CAs
* Predictions: The next observations a CA anticipates
* Prediction errors: Corrections a CA receives about predictions it made
* Predictables: Specifications of what a CA can predict
* Experiences: Syntheses of a CA's past and current observations

Properties/relations directly or indirectly expressed by the above are represented as Origin ---Kind--> Value.

* The origin of a property or relation is an object
* The kind of a property/relation is an atomic name
* The value of a relation is an object
* The value of a property is a number or atom from a domain defined by the property's kind

Observations, Experiences, Predictions and Prediction Errors add meta-data such as `confidence`.

## Kinds of properties/relations

* (sense name) - only when the origin is a sensor
* (action name) - only when the origin is an effector
* (latent property/relation name) - when the property/relation is abduced by a causal theory
* (synthesis name) - either count, more or trend

## Objects in properties/relations

Sensor and effector objects are a priori objects. Latent and synthetic objects are created by CAs as part of their sense making efforts.

* (sensor) -> object{type: sensor, id: (sensor name)}
* (effector) -> object{type: effector, id: (effector name)}
* (latent object) -> object{type:(latent type), id:(unique atom)} - when the object is abduced by a causal theory
* (synthetic object) -> object{type:synthetic, id:(unique atom)} - the id references a list of observations across time frames known only to the CA that synthesized the object

## Properties and relations

A relation is between two objects (its origin and its value). A property is between one object (its origin) and an atomic value.

* origin: (sensor), (effector), (synthetic object), (latent object)
* kind: (sense) e.g. distance, color, contact..., (action) e.g. spin, reverse_spin, count, more, trend, (latent property name), or (latent relation name)
* value: (sense value), (boolean), (integer), many, up, down, same, (latent object) - a value is element of a domain attached to kind

## Experience

* (property or relation)
* confidence: 0.0..1.0
* by: (ca)

## Observation

* (property or relation)
* confidence: 0.0..1.0
* by: (ca)
* of: [(unmwelt_ca), ...]

## Predictable

* origin: (origin)
* kind: (kind)
* domain: (domain) - boolean, [red, green,...], etc.
* by: (ca)

## Prediction

* (property or relation)
* confidence: 0.0..1.0
* by: (ca)
* for: [(unmwelt_ca), ...]

## Prediction error

* prediction: (prediction)
* actual_value: (value)
* confidence: 0.0..1.0
* by: (ca)
