# Wellbeing

## About

Wellbeing is a collection of measures the agent strives to maximize. Wellbeing imparts normativity to beliefs, motivates activity, and focuses attention.

The measures are:

* **Fullness**: How much energy the agent has in store, to "pay for" cognitive effort, effector activation, and (pretend) maintenance and repair.
* **Integrity**: The "health" of the agent, helped by avoiding collisions and not "eating poison"
* **Engagement**: How much the agent is engaging its environment, both by making sense of it and by acting in it

The wellbeing measures are each a pair of numbers, a current value and a gradient.

The current value is an "how much" value computed from aggregating information communicated within Cognition Actors about their computations, actions they take, bumps they suffer, food they "ingest" etc. The gradient value integrates how the current value is changing, that is, how sharply is the value going up or down.

## Signalling wellbeing

Cognition actors (CAs) broadcast wellbeing signals into the society of mind (SOM) once per timeframe, and receive wellbeing signals from other CAs.

Wellbeing signals weaken the further they travel. The distance between two CAs is measured by their degree of umwelt separation, namely the smallest number of edges traversed in a graph connecting CAs via umwelt relationships.

The weaker a signal, the less it nudges the receiving CA's own aggregated wellbeing measure.

Wellbeing signals convey no provenance: "Your wellbeing is my wellbeing, to a point."

At the end of a CA's timeframe (at the end of its periodic OODA-ish loop), a CA adds to/substracts from its own measure of wellbeing based on an accounting of its own "metabolic" work and happenings (bumps, eating...), and the accumulated, attenuated wellbeing signals it received.

The CA adds the updated wellbeing measures to its wellbeing history, enabling it to detect gradients.

## The role of wellbeing

Wellbeing provides the means by which *normativity* is associated with the beliefs of CAs. CAs correlate their wellbeing with beliefs the they synthesize from current and past observations.

Beliefs associated with high and static or with increasing wellbeing measures, are "pleasant" beliefs. Beliefs associated with low and static or with decreasing wellbeing measures are "unpleasant". Beliefs associated with neither are "neutral". Low and decreasing measures feel the worst whereas high and increasing measures feel the best.

Wellbeing drives attention: CAs intend actions to persist pleasant beliefs and actions to terminate unpleasant beliefs. Neutral beliefs are normally "left alone" by the CA but are kept as they may compose the non-neutral beliefs of more abstract CAs.

Wellbeing also provides the motivation for CAs to give birth to new CAs or to remove themselves from the SOM, so as to manage overall energy expenditure or nudge up overall engagement.

### Wellbeing and stress

Stress on a CA is caused by it having low or dropping wellbeing measures.

Stress makes a CA more *plastic*. When stressed, it is more likely to:

* revise its causal model
* temporarily ignore aquired policy habits
* temporarily ignore strongly held beliefs, to act instead on other beliefs
* lower its threshold for action
* trigger its mitosis (birth a new CA) or apoptosis (remove itself from the SOM)

## Fullness

Fullness represents the energy budget of a CA. It starts full.

An agent's collective of CAs is mortal. When there is no energy left, its mind dies (its Lego body is permanent).

Energy is replenished by the action of `eating` but only when the agent is positioned over food (the agent may or may not know it is over food).

Energy is spent individually by each CA when

* obtaining a causal theory (the more time spent searching, the higher the cost of finding the theory)
* synthesizing a belief (each belief comes at a cost)
* using a causal theory (the more complex the theory, the higher the cost per use)
* remembering past observations and beliefs (additional cost per remembered observation/belief)
* completing a time frame (baseline computational/metabolic cost)

Energy is also spent whenever the agent progressively and automatically recovers from lost integrity, i.e. repairs itself.

In response to low and/or decreasing fullness,

A CA may reduce "metabolic costs" by:

* forgetting a past state (oldest first)
* forgetting a belief ignored by all parent CAs (neutral first)
* raising the threshold for persisting/terminating beliefs (don't waste energy on trivial matters!)

## Integrity

Integrity represents the health of the CA. Integrity is initially full.

Integrity decreases because of harmful actions taken by the agent.

Lost integrity is recovered over time but at an energy cost proportional to the amount of recovery.

Integrity is reduced whenever

* the agent's touch sensor is activated, or
* the agent executes the action of `eating` over poison food (the agent may not know to distinguish perceptually between non-food, food and poison but its "metabolism" does).

CAs listen to integrity level events, broadcasted whenever the measure changes significantly.

## Engagement

Engagement keeps track of how engaged the CAs are overall. Engagement is initially empty.

Engagement goes up whenever

* a CA's belief is used in the synthesis of another CA's belief (it becomes relevant), and
* whenever an action it intends is executed (it acts in the world).

Engagement decreases whenever

* a CA's belief loses relevance (it was the basis of another CA's belief that was removed), or
* with the passing of time when no action is executed
