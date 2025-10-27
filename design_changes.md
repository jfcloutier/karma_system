# Design changes

A 1-hour discussion with Elliott Hauser on March 13, 2025 led to a significant rethinking of my design. I thought I'd communicate the changes here prior to revising my design notes.

## Wellbeing

*The concept of Wellbeing actors is retired.*

Cognition actors (CAs) broadcast wellbeing signals into the society of mind (SOM) and receive wellbeing signals from other CAs.

Wellbeing signals weaken the further they travel. The distance between two CAs is measured by their degree of umwelt separation, namely the smallest number of edges traversed in a graph connecting CAs via umwelt relationships.

The weaker a signal, the less it nudges the receiving CA's own aggregated wellbeing measure.

Wellbeing signals convey no provenance: "Your wellbeing is my wellbeing, to a point."

At the end of a CA's timeframe (at the end of its periodic OODA-ish loop), a CA adds to/substracts from its own measure of wellbeing based on an accounting of its own "metabolic" work and happenings (bumps, eating...), and the accumulated, attenuated wellbeing signals it received.

The CA adds the updated wellbeing measures to its wellbeing history, enabling it to detect gradients.

## Stress

Stress on a CA is caused by it having low or dropping wellbeing measures.

Stress makes a CA more *plastic*. When stressed, it is more likely to:

* revise its causal model
* temporarily ignore aquired habits (e.g. affordances)
* temporarily ignore strongly held experiences, to act instead on other experiences
* lower its threshold for action
* trigger its mitosis or apoptosis

## Mitosis and apoptosis

*The concept of "meta-cognition actors" is retired.*

The SOM grows and shrinks, exploring a space of configurations, searching for competent (life-sustaining) configurations. The SOM grows via "mitosis" (CA birth) and shrinks via "apoptosis" (CA death).

CAs beget other CAs (mitosis) and CAs remove themselves (apoptosis) all on their own. "Meta-cognition" actors are no longer required or involved.

### Mitosis

At the end of its current timeframe, a CA at abstraction level L might add another CA to the SOM, at its own level **or** one level up, but not both.

Whether or not a CA is added or removed is probabilistic and dependent on the circumstances of the SOM.

When a CA is added, it starts with initial wellbeing measures:

* maximum fullness
* maximum integrity
* mimimum engagement

#### Adding a CA one level up

With a probability proportional to the CA's fullness (modulated up by stress):

If:

* level L+1 is empty of CAs and all level L-1 CAs are in umwelts and
* the CA attempting mitosis is not in any umwelt and can recruit 1 or more CAs at level L

Then:

* the mitotic CA creates a CA at level L+1 with itself and the recruited CAs as its umwelt.

#### Adding a CA at the same level

With a probability proportional to the CA's fullness (modulated up by stress):

If:

* A level L+1 CA was not created and
* the mitotic CA can recruit 1 or more CAs at level L-1 not in its umwelt and
* the CA's resulting transitive umwelt is uniquely specialized (see Holarchy and specialization below)

Then:

* the mitotic CA creates a CA at its level L with an umwelt composed of the recruited CAs plus one or more of its own, randomly chosen, umwelt CAs.

#### Recruiting a CA

When a CA is asked to join an umwelt as part of the mitosis of another CA, it either accepts or refuses with  probability modulated by its state.

It refuses being recruited if it does not yet have a causal model.

The probability that it accepts goes down:

* the more it participates in umwelts already (it converges to 0 rather quickly)
* the lower its wellbeing, modulated up by stress

### Apoptosis

At the end of its current timeframe, a CA at level L might undergo apoptosis (remove itself from the SOM), with a probability inversely proportional to the CA's fullness, modulated up by stress:

If:

* It's wellbeing measures are low or consistently dropping
* The CA is dispensable to all level L+1 CAs (i.e. none of its experiences uniquely supports a level L+1 experience)

Then:

* It removes itself from the SOM

## Parameterizing exploration vs exploitation

Each CA is on an exploration-exploitation spectrum as defined by its responsiveness to stress.

An exploitation tendency corresponds to low responsiveness to stress (the CA tends to "stay the course" even when stressed).

An exploration tendency corresponds to high responsiveness to stress (the CA tends to "mix things up" when stressed).

A CA's responsiveness to stress is set once, when it is added to the SOM. It is set with probabilities designed to generate a gaussian distribution across all CAs, whereby most CAs more or less balance exploration vs exploitation.

## Holarchy and specialization

The CAs in the SOM is no longer referred to as composing a *hierarchy* but, more accurately, a *holarchy*. This provides a better framework for the concept of *specialization* within the SOM.

> "Holarchy: a whole that is a part of other wholes, while simultaneously containing parts that are whole in themselves." - Arthur Koestler

A CA can be viewed as the interface to a "holon", i.e. a *functional* collective of CAs made up by its transitive umwelt and thus capable of acting as a unit (e.g. the heart, is a collective of bundles of cells that together pump blood). The transitive umwelt of a CA are all the CAs in its immediate uumwelt, plus the transitive umwelts of these CAs.

A holarchy emerges over time from CA mitosis, organized around the agent's physical sensors and effectors.

A CA is singled out as **specialized** if its umwelt transitively controls a *unique* set of sensors and effectors.

At most one CA *per level of the SOM* is allowed to control any one set of sensors and effectors. It is unique, at a given level of abstraction, in having experiences and affordances covering a given sensorium (set of sensors) and effedorium (set of effectors).
