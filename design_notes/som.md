# SOM

## Structure

The SOM is a hierarchichal collective of cognition actors (CAs) that animate an agent.

## Cognition Actors

Each CA has an umwelt composed of a small number of CAs from one level below.

A CA synthesizes its beliefs from patterns detected in the observed/predicted beliefs, past and present, of the CAs in its umwelt.

The beliefs of a CA exist in the context of wellbeing measures, current and trending. The wellbeing measures are `fullness`, `integrity` and `engagement`. They signal risks, present or absent, to the survivability of the CA and. possibly, the entire collective of CAs.

Beliefs associated with high risks are unpleasant. Beliefs associated with low risks are pleasant. Others are neutral. A CA acts on its umwelt in response to the pleasantness or unpleasantness of its current beliefs in order to change or preserve them. It does so by impacting beliefs in its umwelt from which its own beliefs are derived.

## Growth and shrinking

The SOM grows and shrinks, exploring a space of configurations of CAs, searching for competent (life-sustaining) configurations. The SOM grows via "mitosis" (CA birth) and shrinks via "apoptosis" (CA death).

CAs beget other CAs (mitosis) and CAs remove themselves (apoptosis).

### Mitosis

At the end of its current timeframe, a CA at abstraction level L might birth another CA, at its own SOM level **or** one level up, but not both.

Whether or not a CA is added or removed is probabilistic and dependent on the circumstances of the SOM.

When a CA is added by another, it starts with these wellbeing measures:

* half the fullness of its originator CA
* the integrity of its originator CA
* mimimum engagement

#### Adding a CA one level up

This is done with a probability proportional to the CA's fullness (modulated up by stress).

If:

* the level above is empty of CAs and all CAs at the level below are in umwelts and
* the CA attempting mitosis can recruit 1 or more CAs at at its level to be with it in the umwelt of the newly created CA one level above

Then:

* the mitotic CA creates a CA one level above with itself and the recruited CAs as its umwelt.

#### Adding a CA at the same level

This is done with a probability proportional to the CA's fullness (modulated up by stress):

If:

* A level L+1 CA was not created in the current timeframe and
* the mitotic CA can recruit 1 or more CAs at level L-1 not in its umwelt and
* the CA's resulting transitive umwelt is uniquely specialized (see Holarchy and specialization below)

Then:

* the mitotic CA creates a CA at its level L with an umwelt composed of the recruited CAs plus one or more of its own, randomly chosen, umwelt CAs.

#### Recruiting a CA

When a CA is asked to join an umwelt as part of the mitosis of another CA, it either accepts or refuses with probability modulated by its state.

It refuses being recruited if it does not yet have a symbolic generative model (a.k.a causal theory).

The probability that it accepts goes down:

* the more it participates in umwelts already (it converges to 0 rather quickly)
* the lower its wellbeing

### Apoptosis

At the end of its current timeframe, a CA at level L might undergo apoptosis (remove itself from the SOM), with a probability inversely proportional to the CA's fullness, modulated up by stress:

If:

* It's wellbeing measures are low or consistently dropping
* The CA is dispensable to all level L+1 CAs (i.e. none of its beliefs uniquely supports a level L+1 belief)

Then:

* It removes itself from the SOM
* after dispersing its fullness to its parents

## Parameterizing exploration vs exploitation

Each CA is on an exploration-exploitation spectrum as defined by its responsiveness to stress.

An exploitation tendency corresponds to low responsiveness to stress (the CA tends to "stay the course" even when stressed).

An exploration tendency corresponds to high responsiveness to stress (the CA tends to "mix things up" when stressed).

The parameters that determine a CA's responsiveness to stress are set once, when it is added to the SOM. They are set separately for each CA with probabilities designed to generate a gaussian distribution across all CAs, whereby most CAs begin and go though their entire lives with a set balance between exploration vs exploitation tendencies.

## Holarchy and specialization

The CAs in the SOM can be referred to as composing a *hierarchy* but, more accurately, as constituting a *holarchy*. This provides a better framework for the concept of *specialization* within the SOM.

> "Holarchy: a whole that is a part of other wholes, while simultaneously containing parts that are whole in themselves." - Arthur Koestler

A CA can be viewed as the interface to a "holon", i.e. a *functional* collective of CAs made up by its transitive umwelt and thus capable of acting as a unit (e.g. the heart, is a collective of bundles of cells that together pump blood). The transitive umwelt of a CA are all the CAs in its immediate umwelt, plus the transitive umwelts of these CAs.

A holarchy emerges over time from CA mitosis, organized around the agent's physical sensors and effectors.

A CA is singled out as **specialized** if its umwelt transitively controls a *unique* set of sensors and effectors.

At most one CA *per level of the SOM* is allowed to control any one set of sensors and effectors. It is unique, at a given level of abstraction, in having beliefs and policies covering a given sensorium (set of sensors) and effedorium (set of effectors).

## Communication between CAs

The CAs form a collective which implies there is communication between them to enable coordination, cooperation, competition etc.

Most communications are between a CA and its umwelt CAs and vice-versa. Other communications span the entire collective.

Communications are done either via broadcasted events that CAs either listen to or ignore, or via directed messages.

### CA to umwelt CAs

* Predictions - beliefs expected to be held by at least some umwelt CAs
* Directives - prioritized goals to achieve (the CA receiving the directive is free to choose how)

### Unwelt CAs to parent CAs

* Beliefs domain - what predicates are used to express beliefs, and their value domains (so the parent CAs knows how to compose predictions, irrespective of its causal theory)
* Prediction errors - contradicting received predictions
* Action reports - whether a directive can be actualized, is ready to actualize or was successful
* Lifecycle - notifying the parent of being added to, or removed from, its umwelt

### CA to all CAs

* Wellness measure change - broadcasted whenever a CA's fullness, integrity or engagement mesaure changes. See notes on wellbeing for details about the "diffusion" of wellbeing information across the SOM

## Contraints

* Bottom-up constraints
  * Umwelt CAs determine what their parents can observe and do. They...
    * determine the set of beliefs the level parent CAs can observe, build causal theories from, and compose into abstract beliefs
    * determine set of meaningful goals in a parent CA's policy
* Top-down constraints
  * A CA models its umwelt CAs but not vice-versa
    * umwelt CAs can't make sense of why they are directed to impact their beliefs - they simply accept it (Froese's Irruption Theory?)
  * A CA reduces the agency of its umwelt
    * it imposes directives (policies to execute or goals to achieve) on umwelt CAs to achieve its own goals
      * umwelt CAs however decide how to fulfill received directives (they are not micromanaged, just directed)
      * but they can't fulfill their own goals while fulfilling their parent CA's goals
      * and they have fewer opportunity to intend their own goals and work on being/staying relevant
  * A CA is in a better position than its umwelt to keep the agent alive if
    * it can detect the more abstract observation patterns that are more likely to correlate with wellbeing trends
    * and thus can set goals (to initiate/persist/terminate its beliefs) that will be more effective at maintaining the entire SOM alive
  * A CA restricts the causal theory search space of its umwelt CAs (by imposing restriction on the vocabulary used)
    * umwelt CAs can not "unground" parent CA's beliefs (by disappearing the vocabulary of umwelt beliefs used by the parent CAs to synthesize abstract beliefs)
    * this imposes constraints on the abduced objects/predicates in the signatures of causal theories
