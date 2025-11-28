# SOM

## Structure

The SOM is a hierarchichal collective of cognition actors (CAs) that animate an agent.

## Cognition Actors

Each CA has an umwelt composed of a small number of CAs from one level below.

A CA synthesizes its experiences from patterns detected in the observed/predicted experiences, past and present, of the CAs in its umwelt.

The experiences of a CA exist in the context of wellbeing measures, current and trending. The wellbeing measures are `fullness`, `integrity` and `engagement`. They signal risks, present or absent, to the survivability of the CA and. possibly, the entire collective of CAs.

Experiences associated with high risks are unpleasant. Experiences associated with low risks are pleasant. Others are neutral. A CA acts on its umwelt in response to the pleasantness or unpleasantness of its current experiences in order to change or preserve them. It does so by impacting experiences in its umwelt from which its own experiences are derived.

## Growth and shrinking

See [Searching morphospace](./searching%20morphospace.md)

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

At most one CA *per level of the SOM* is allowed to control any one set of sensors and effectors. It is unique, at a given level of abstraction, in having experiences and plans covering a given sensorium (set of sensors) and effedorium (set of effectors).

## Communication between CAs

The CAs form a collective which implies there is communication between them to enable coordination, cooperation, competition etc.

Most communications are between a CA and its umwelt CAs and vice-versa. Other communications span the entire collective.

Communications are done either via broadcasted events that CAs either listen to or ignore, or via directed messages.

### CA to umwelt CAs

* Predictions - experiences expected to be held by at least some umwelt CAs
* Directives - prioritized goals to achieve (the CA receiving the directive is free to choose how)

### Unwelt CAs to parent CAs

* Experiences domain - what predicates are used to express experiences, and their value domains (so the parent CAs knows how to compose predictions, irrespective of its causal theory)
* Prediction errors - contradicting received predictions
* Action reports - whether a directive can be actualized, is ready to actualize or was successful
* Lifecycle - notifying the parent of being added to, or removed from, its umwelt

### CA to all CAs

* Wellness measure change - broadcasted whenever a CA's fullness, integrity or engagement mesaure changes. See notes on wellbeing for details about the "diffusion" of wellbeing information across the SOM

## Contraints

* Bottom-up constraints
  * Umwelt CAs determine what their parents can observe and do. They...
    * determine the set of experiences the level parent CAs can observe, build causal theories from, and compose into abstract experiences
    * determine set of meaningful goals in a parent CA's plan
* Top-down constraints
  * A CA models its umwelt CAs but not vice-versa
    * umwelt CAs can't make sense of why they are directed to impact their experiences - they simply accept it (Froese's Irruption Theory?)
  * A CA reduces the agency of its umwelt
    * it imposes directives (goals to achieve) on umwelt CAs to achieve its own goals
      * umwelt CAs however decide how to fulfill received directives (they are not micromanaged, just directed)
      * but they can't fulfill their own goals while fulfilling their parent CA's goals
      * and they have fewer opportunity to intend their own goals and work on being/staying relevant
  * A CA is in a better position than its umwelt to keep the agent alive if
    * it can detect the more abstract observation patterns that are more likely to correlate with wellbeing trends
    * and thus can set goals (to initiate/persist/terminate its experiences) that will be more effective at maintaining the entire SOM alive
  * A CA restricts the causal theory search space of its umwelt CAs (by imposing restriction on the vocabulary used)
    * umwelt CAs can not "unground" parent CA's experiences (by disappearing the vocabulary of umwelt experiences used by the parent CAs to synthesize abstract experiences)
    * this imposes constraints on the abduced objects/predicates in the signatures of causal theories
