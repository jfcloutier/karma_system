# Wellbeing

## About

Wellbeing is a collection of measures the agent strives to maximize. Wellbeing imparts normativity to beliefs, motivates activity, and focuses attention.

The measures are:

* **Fullness**: How much energy the agent has in store, to "pay for" cognitive effort, effector activation, and (pretend) maintenance and repair.
* **Integrity**: The "health" of the agent, helped by avoiding collisions and not "eating poison"
* **Engagement**: How much the agent is engaging its environment, both by making sense of it and by acting in it

In additions to current measures of wellbeing, a CA also keeps track of the rising and falling of these measures. A sharply falling, yet still high, measure of a CA's wellbeing can be as "alarming" as a low measure.

The wellbeing measures of a CA grow and decrease based on actions they take, bumps they suffer, food they "ingest" etc. They also change from CAs sharing their individual wellbeings as they diffuse across the collective of CAs.

## The role of wellbeing

Wellbeing provides the means by which *normativity* is associated with the beliefs of CAs. CAs correlate their wellbeing with beliefs they synthesize from current and past observations.

Beliefs associated with high and static or with increasing wellbeing measures, are "pleasant" beliefs. Beliefs associated with low and static or with decreasing wellbeing measures are "unpleasant". Beliefs associated with neither are "neutral". Low and decreasing measures feel the worst whereas high and increasing measures feel the best.

Wellbeing drives attention: CAs intend actions to persist pleasant beliefs and actions to terminate unpleasant beliefs. Neutral beliefs are normally "left alone" by the CA but are kept as they may compose the non-neutral beliefs of more abstract CAs.

Wellbeing also provides the motivation for CAs to spawn new CAs or to remove themselves from the SOM, so as to manage overall energy expenditure or nudge up overall engagement.

### Wellbeing and stress

Stress on a CA is caused by it having low or dropping wellbeing measures.

Stress makes a CA more *plastic*. When stressed, it is more likely to:

* revise the causal theory it uses as a symbolic generative model
* temporarily ignore aquired policy habits
* temporarily ignore strongly held beliefs, to act instead on other beliefs
* lower its threshold for action
* trigger its mitosis (birth a new CA) or apoptosis (remove itself from the SOM)

## Measures of wellbeing

### Fullness

Fullness represents the energy budget of a CA. It starts full.

An agent's collective of CAs is mortal. When there is no energy left, its mind dies (its Lego body is permanent).

Energy is replenished by the action of `eating` but only when the agent is positioned over food (the agent may or may not know it is over food).

Energy is spent individually by each CA when

* obtaining a causal theory (the more time spent searching, the higher the cost of finding the theory)
* synthesizing a belief (each belief comes at a cost)
* using a causal theory (the more complex the theory, the higher the cost per use)
* remembering past observations and beliefs (additional cost per remembered observation/belief)
* completing a timeframe (baseline computational/metabolic cost)

Energy is also spent whenever the agent progressively and automatically recovers from lost integrity, i.e. repairs itself.

In response to low and/or decreasing fullness,

A CA may reduce "metabolic costs" by:

* forgetting a past state (oldest first)
* forgetting a belief ignored by all parent CAs (neutral first)
* raising the threshold for persisting/terminating beliefs (don't waste energy on trivial matters!)

### Integrity

Integrity represents the health of the CA. Integrity is initially full.

Integrity decreases because of harmful actions taken by the agent.

Lost integrity is recovered over time but at an energy cost proportional to the amount of recovery.

Integrity is reduced whenever

* the agent's touch sensor is activated, or
* the agent executes the action of `eating` over poison food (the agent may not know to distinguish perceptually between non-food, food and poison but its "metabolism" does).

CAs listen to integrity level events, broadcasted whenever the measure changes significantly.

### Engagement

Engagement keeps track of how engaged the CAs are overall. Engagement is initially empty.

Engagement goes up whenever

* a CA's belief is used in the synthesis of another CA's belief (it becomes relevant), and
* whenever an action it intends is executed (it acts in the world).

Engagement decreases whenever

* a CA's belief loses relevance (it was the basis of another CA's belief that was removed), or
* with the passing of time when no action is executed

## Spreading wellbeing

The wellbeing of cognition actors (CAs) diffuse throughout the society of mind (SOM) as if by osmosis.

Wellbeing signals are realized by wellbeing tokens, created and destroyed, that travel between CAs without provenance info ("Your wellbeing is my wellbeing, to a point".)

The tokens diffuse down gradients across umwelt relationships, that is with parents and umwelt. Within a timeframe, a CA consumes or produces wellbeing tokens depending on its activies (e.g. getting a new causal theory) and happenings (e.g. touch sensor bumped). At the end of a timeframe, some tokens held by a CA disappear if expired. Some of the remaining tokens (randomly chosen) diffuse, by type, down to umwelt CAs and or up to parent CAs to equilibrate (eliminate the gradient).

Once a CA has equilibrated its wellbeing tokens with its entourage (i.e. parents and umwelt), it adds up wellbeing tokens it holds to compute its wellbeing measures by type. It keeps a snapshot in its timeframe history, enabling it to determine its wellbeing trends.

### Modulating the sharing of wellbeing

A CA can modulate the wellbeing of its umwelt by temporarily misrepresenting to its umwelt (and only its umwelt) the number of wellbeing tokens it holds .

A CA can do so by claiming to all its umwelt CAs that:

* it has no token of a given type, thus acting as a hoarder, taking half the tokens from each umwelt CA at the end of each timeframe
* it has as many tokens of a given type thus always declining tokens from its umwelt

Any CA with can change its wellbeing representation toward its umwelt. It is an action the CA can take as part of a policy it constructs to impact a belief it holds. The action changes how it presents its wellbeing levels to its umwelt.

The actions are:

* hoard(wellbeing_type)
* decline(wellbeing_type)
* share(wellbeing_type)

 The change persists until further action. A CA starts life sharing its fullness, integrity and engagement wellbeing tokens.
