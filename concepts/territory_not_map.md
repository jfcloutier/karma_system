# The Artificial Agency territory is not the Active Inference map

The project ontology differs from the Active Inference ontology because it is about how I am building a territory (an implementation of robotic agency), whereas the Active Inference ontology is about an implementation-agnostic way of mapping the realized territory.

A Being, as defined in the ontology, is not homeostatic but rather rheostatic in that it is the Being's continuity of change that is preserved, not any specific, composite state, however long-lived that state may be. This is important since, in my implementation of agency, a collective of cognition actors (each actor is a stateful process) is in constant flux, as higher-level processes search a space of possible configurations of the collective for competent (i.e. survivable) ones.

In my implementation of agency, I have two ways of capturing regularities, namely causal theories and temporal patterns. None are Bayesian in nature.

Causal theories generalize sequences of remembered observations into rules, rules about what could be observed at once and what ought to be observed next. 

Temporal patterns are facts detected in sequences of remembered observations, for example, the existence of a downward trend in the observed distances to an obstacle, or the interruption of this trend.

Note that, in my design, I call these (felt) temporal patterns "experiences", which can be confusing since they represent only one type of regularities, the other being symbolic generative models.

Also note that the temporal patterns detected by a cognition actor become observations available to cognition actors one level up. The higher-level cognition actors would then examine these "elevated" observations for more abstract rules and temporal patterns.
