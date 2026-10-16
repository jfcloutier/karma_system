# Cognition actors

A CA strives to become increasingly competent at surviving by making sense of its umwelt and taking actions beneficial to its wellbeing.

A CA makes sense of its umwelt (a few lower-level CAs) by predicting changes to it (i.e. predicting incoming observations of its umwelt CAs' percepts) and by abstracting its own percepts from observations of its umwelt. Its percepts become observations available to parent CAs (higher-level CAs that have the CA in their umwelts).

A CA is effective at impacting its umwelt if it has reliable affordances it can apply to validate pleasant percepts or invalidate unpleasant percepts. A percept is pleasant if it was derived in the context of high or improving wellbeing, unpleasant in the context of low or worsening wellbeing.

The more competent a CA is, the more likely it is that its parents CAs will be competent and survive, and thus the more likely it is that the CA itself will survive; orphaned CAs are susceptible to removing themselves when wellbeing is consistently low.

## Types of cognition actors

There are two broad types of cognition actors, dynamic CAs and static CAs.

Static CAs -sensor CAs and effector CAs- are determined a priori by the sensors and effectors that are on the agent's body. They populate the bottom layer of the Society Of Mind (SOM) and persist throughout the life of the SOM.

Dynamic CAs populate all other layers of the SOM and are added and removed throughout the life of the agent as it searches the space of SOM configurations for one that, at the very least, keeps it alive.

Dynamic CAs have umwelts and they have causal theories to make sense of their observations of their umwelts. A static CAs have neither.

## Timeframe and memory

A CA operates one timeframe after another. The current timeframe of a CA corresponds to a "thick now"; all observations made and all percepts abstracted by the CA during this timeframe are considered synchronous. Timeframes are not synchronized across CAs. The timeframe of a CA starts and stops independently of those of other CAs. The current timeframes of CAs partially and randomly overlap.

During its current timeframe, a CA makes new observations by predicting the latest percepts of CAs in its umwelt, updating its wellbeing measures, refreshing its set of percepts by integrating the latest observations with past ones, and assigning up-to-date normative values (pleasantness/unpleasantness) to its current percepts.

At the end of the current timeframe, a CA decides whether to act on its updated percepts and, if so, how.

Upon completing its current timeframe, a CA adds the state of the timeframe to its memory of past states. The CA uses its remembered past states to compute its wellbeing gradients, derive current (pleasant vs unpleasant) percepts, and update the causal theory that explains its past observations and predicts incoming ones.

There is a "metabolic" cost associated with memory. The higher a CA's metabolic costs, the faster its fullness wellbeing drains. A CA under stress from low fullness might reduce the size of its memory to reduce this drain. Regaining high fullness would restore the prior bound on the CA's memory size.

CAs higher up in the collective's hierarchy have qualitatively longer timeframes and longer memories (more states are remembered). They are also a greater draw on fullness.
When the maximum number of remembered states is reached and the latest state is committed to memory (upon completion of the current timeframe), the oldest state is dropped from memory.

## Observing (its umwelt's percepts)

* A (dynamic) CA predicts its observations of percepts of CAs in its umwelt
  * A CA begins life with an empty causal theory that predicts random, domain-bounded observations or prior observations.
  * If the CA has a causal theory, it uses it to predict the next observations.
* A CA predicts the success of its plans using its causal theory. It also remembers the effecticeness of previously executed plans.
* If a prediction is met with a prediction error, the prediction error becomes the latest observation, else the uncontested prediction is the observation.
* A CA drops repeated states (state = observations in the same timeframe) - i.e. a CA's perceived time stands still while its umwelt does not appear to change.

* See [predicting_and_observing.md](./predicting_and_observing.md)

## Understanding (relating observations causally and via constraints)

* To be competent, a CA needs to make sense of its observations via a causal theory of
  * how its umwelt changes on its own
  * how its umwelt changes from the CA executing plans
* A CA requests a causal theory from the Apperception Engine when
  * it has no theory and a theory could be generated from its remembered states
  * it has a theory and its predictive capabilities have degraded since acquired such that it is no longer good enough
  * it has a theory but has had new plans executed since the theory was generated

* A CA's causal theory makes causal sense of percepts observed in its umwelt
  * necessary co-occurrences of observations from static rules
    * if a static rule states "A whenever B and C:, then observing B and C at time T infers (deductively) observing A also at T
    * e.g if the proximity got smaller then the ambient light must also have gotten brighter
  * sequencing of observations from causal rules
    * if a causal rule states "A after B and C", then
      * observing A at time T entails (abductively) B and C at T-1
      * having observed B and C at T-1 entails (deductively) A at time T
    * e.g. the color will become gray if the color is green and both wheels spin

* The CA applies the theory's causal rules to predict the next state so it can predict umwelt percepts
  * from the considered execution of an plan selected to achieve an intent (impacting a held percept)
  * due to "spontaneous" changes in the umwelt

## Perceiving (detecting patterns of change in observations)

* A sensor CA has atomic percepts obtained from sensor readings
* A dynamic CA gets its percepts
  * by composing observed, umwelt percepts into synthetic percepts
  * by aggregating directive activations percepts (observed in the umwelt) into percepts of the activation of its own, planned, goals

* See [perceiving.md](./perceiving.md)

## Acting (on felt percepts)

* A CA seeks to validate a pleasant percept and invalidate an unplesant percept
  * By furthering or interrupting (i.e. impacting) sub-percepts via intents delegated to umwelt CAs
* Realizing an intent is recursive because a percept is a recursive structure of percepts held by umwelt CAs

* See [planning.md](./planning.md) and [acting.md](./acting.md)

## Attention

* A percept, when synthesized, is associated with a feeling based on wellbeing/pleasantness trend (better, worse, same)
  * A CA remembers the ambient wellbeing at each timeframe
* A CA attends to strongly felt percepts, those associated with distinctly low/high or dropping/increasing wellbeing
* Higher-level percepts are expected to be more likely associated with clear wellbeing trends than lower-level percepts
  * This drives the SOM to add levels until clear wellbeing trends appear that productively drive attention
  * Afforded control over wellbeing makes up for the higher resource consumption of added SOM levels

  See [feeling.md](./feeling.md)

## Wellbeing

* A CA starts life with half the fullness of its mitotic progenitor, full integrity and no engagement
* A CA updates its wellbeing measures (fullness, integrity and engagement):
  * They are restored/depleted by the actions of the agent and by the passage of time
  * Wellbeing fullness is osmotically equilibrated among CAs over parent-umwelt links

* See [wellbeing.md](./wellbeing.md)

## The lifecycle of a cognition actor

The lifecycle of a dynamic CA (sensor and effector CAs are static) is a sequence of time frames.
Each time frame goes through phases driven by messages the CA sends itself to progress from one to the next.

The lifecycle of a dynamic CA ends when the CA decides to terminate itself.

At any phase in a time frame, the CA immediately processes all events and messages from other CAs and updates its state.

The phases of a time frame are:

* beginning         - persist recently received predictions
* predicting       - make predictions from current observations
* observing       - merge predictions and prediction errors into new observations
* perceiving    - integrate current and past observations into terminated, updated and new percepts
* feeling          - assign a normative value (from worst to best feeling) to each percept
* acting           - formulate, accept and prioritize goals to impact strongly felt percepts, make plans to achieve goals and execute them
* assessing        - evaluate causal theory and request new one if unsatisfactory, evaluate executed plans as affordances from whether and when their goals were achieved, abandon stale goals, update and diffuse wellbeing fullness (create cognitive glue), mitosis/apoptosis

```mermaid
---
title: The phases of each timeframe of a Cognition Actor
---
stateDiagram-v2
    [*] --> beginning : Create a new CA with an umwelt
    beginning --> predicting: Persist recently received predictions
    predicting --> observing: Make predictions about umwelt percepts
    observing --> perceiving: Merge predictions and prediction errors into new observations
    perceiving --> feeling: Unify observations into percepts
    feeling --> acting: Make percepts feel good or bad
    acting --> assessing: Formulate and execute plans to impact percepts
    assessing --> beginning: Evaluate competency of causal model and past plans, review active goals, diffuse fullness, choose how to go on
    assessing --> [*]: Choose to terminate self
```
