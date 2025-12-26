# Representing properties and relations

Experiences, Predictions, Prediction Errors, Predictables and Observations of CAs are about properties or relations.

They represent different perspectives held by CAs about properties/relations.

Properties/relations are represented as Origin ---Kind--> Value.

* The origin of a property or relation is an object
* The kind of a property/relation is an atomic name
* The value of a relation is an object
* The value of a property is a number or atom from a domain associated to the property's kind

Prediction Errors are about Predictions, which are about properties/relations.

Experiences, Predictions, Prediction Errors Predictables and Observations add meta-data such as confidence.

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
* (synthetic object) -> object{type:synthetic, id:(unique atom)} - the id references a list of objects across time frames known only to the CA that synthesized the object

## Experience

Property/relation:

* kind: (sense) e.g. distance, color, contact..., (action) e.g. spin, reverse_spin, count, more, trend, (latent property name), (latent relation name)
* origin: (sensor), (effector), (specs of a sequence or set of observations), (latent object)
* value: (sense value), (boolean), (integer), many, up, down, same, (latent object) - a value is element of a domain attached to kind

Meta data:

* confidence: 0.0..1.0
* by: (ca)

## Observation

* kind, origin, value, confidence, by
* of: [(unmwelt_ca), ...]

## Predictable

* kind, origin, by
* domain: (domain) - boolean, [red, green,...], etc.

## Prediction

* kind, origin, value, confidence, by
* for: [(unmwelt_ca), ...]

## Prediction error

* confidence, by
* prediction: (prediction)
* actual_value: (value)
