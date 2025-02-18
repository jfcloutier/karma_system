# Ontology

**Being**:
> A metastable system of processes achieving [constraint closure](https://montevil.org/publications/articles/2015-mm-organisation-closure-constraints/) (a *living* being is additionally self-producing)

**Umwelt** (the being's):
> All that is not the **being**, and can change the being or be changed by it (the being's outer-world)

**Innenwelt**:
> Changes to the **being** available to its **sentience** (the being's inner-world)

**Sentience**:
> Processes of **being** integrating *durable changes* to the **innenwelt**, causing further changes to the being and then, possibly and as a consequence, to its **umwelt**

**Feelings**:
> Durable changes to the **innenwelt** (such changes are always caused by the **being**'s processes) that stand for measures of the being's precariousness (feelings of low precariousness are good feelings)

**Experiences**:
> Durable changes to the **innenwelt** that stand for prior changes to the innenwelt correlated with **feelings**

**Beliefs**:
> Durable changes to the **innenwelt** that stand for regularities, or loss thereof, in **experiences**

**Consciousness**:
> **Experiences** of **sentience**

**Agent**:
> A **sentient** **being**, possibly **conscious**, who changes itself and its **umwelt** (i.e. acts) in accordance to its **beliefs**, promoting experiences that feel good

This differs from the Active Inference ontology because it is about how I am building a territory (an implementation of robotic agency), whereas the Active Inference ontology is about an implementation-agnostic way of mapping the realized territory.

A Being, as defined above, is not homeostatic but rather rheostatic in that it is the Being's continuity of change that is preserved, not any specific, composite state, however long-lived that state may be. This is important since, in my implementation of agency, a collective of cognition actors (each actor is a stateful process) is in constant flux, as higher-level processes search a space of possible configurations of the collective for competent (i.e. survivable) ones.

In my implementation of agency, I have two ways of capturing regularities, namely causal theories and temporal patterns.

Causal theories generalize sequences of remembered observations into rules, rules about what could be observed at once and what ought to be observed next. 

Temporal patterns are facts detected in sequences of remembered observations, for example, the existence of a downward trend in the observed distances to an obstacle, or the interruption of this trend.

Note that, in my design, I call these (felt) temporal patterns "beliefs", which can be confusing since they represent only one type of regularities, the other being causal models.

Also note that the temporal patterns detected by a cognition actor become observations available to cognition actors one level up. The higher-level cognition actors would then examine these "elevated" observations for more abstract rules and temporal patterns.