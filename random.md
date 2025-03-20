# Random notes

## Wellbeing

There are no Wellbeing actors; CAs send wellbeing signals and receive wellbeing signals from other CAs.

Wellbeing signals weaken the further they travel. The distance between CAs is measured by their degree of (umwelt) separation.

Wellbeing signals convey no provenance: Your wellbeing is my wellbeing, to a degree.

At the end of a timeframe, a CA

* adds to/substracts from its own measure of wellbeing based on an accounting of its own "metabolic" work and happenings (bumps, eating...), and the attenuated wellbeing signals it received
  * the weaker a signal, the less it nudges the receiving CA's own wellbeing measure
* adds to its history of its fluctuating wellbeing to detect gradients

## Stress

Stress to a CA is caused by it having low or dropping wellbeing measures

Stress makes a CA more *plastic*, i.e. when stressed, it is more likely to

* revise its causal model
* temporarily ignore aquired policy habits
* temporarily ignore strongly held beliefs to act instead on other beliefs
* lower its threshold for action
* trigger its mitosis or apoptosis

## Mitosis and apoptosis

CAs beget other CAs (mitosis) and CAs remove themselves (apoptosis) on their own; no external actors are required or involved.

### Mitosis

At the end of its current timeframe, a CA at level L attempts to add another CA to the SOM, at its own level **or** one level up.

The CA is added with starting wellbeing measures:

* maximum fullness
* maximum integrity
* mimimum engagement

#### One level up

With a probability proportional to the CA's fullness (modulated up by stress)

If

* level L+1 is empty and all level L-1 CAs are in umwelts and
* the CA is not in any umwelt and can recruit 1 or more CAs at level L

Then

* it creates a CA at level L+1 with itself and the recruited CAs as its umwelt

#### Same level

With a probability proportional to the CA's fullness (modulated up by stress)

If

* A level L+1 CA was not created and
* the CA can recruit 1 or more CAs at level L-1 not in its umwelt

Then

* it creates a CA at level L with an umwelt composed of the recruited CAs plus one or more of its own, randomly chosen, umwelt CAs

#### Recruiting a CA

When a CA is asked to join an umwelt, it either accepts or refuses.

It refuses if it does not yet have a causal model

The probability that it accepts goes down

* the more it participates in umwelts already (it converges to 0 rather quickly)
* the lower its wellbeing, modulated by stress

### Apoptosis

At the end of its current timeframe, a CA at level L attempts to remove itself from the SOM.

With a probability inversely proportional to the CA's fullness (modulated up by stress)

If

* The CA is not relevant to a level L+1 CA
  * i.e. none of its beliefs support a level L+1 belief

## Parameterizing exploration vs exploitation

Each CA is on an exploration-exploitation spectrum as defined by its responsiveness to stress

* Exploitation corresponds to low responsiveness
* Exploration corresponds to high responsiveness
* Responsiveness to strees is set at mitosis
  * with probabilities designed to generate a gaussian distribution across all CAs

## Illusions

TBD

## Holarchy and specialization

> "Holarchy: a whole that is a part of other wholes, while simultaneously containing parts that are whole in themselves." - Arthur Koestler

* A CA can be the interface for a functional collective of CAs
  * A singular collective that acts as one unit (the heart, as a collective of cells, pumps blood)
* A holarchy emerges over time from CA mitosis in the SOM
  * It organizes around primitive *categories of effects*
    * moving, eating, intro-effecting
  * A CA is singled out as **specialized** if its umwelt transitively gives it control over one or more complete categories of effectors (e.g. all moving effectors and all eating effectors)
  * At most one CA in the SOM can control a given set of effector categories
  * Thus only it can have policies covering this set of effector categories
