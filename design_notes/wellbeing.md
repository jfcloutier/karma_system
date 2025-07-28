# Wellbeing

## About

Wellbeing is a collection of measures the agent strives to maximize. Wellbeing imparts normativity to beliefs, motivates activity, and focuses attention.

The measures are:

* **Fullness**: How much energy the agent has in store, to "pay for" cognitive effort, effector activation, and health recovery
* **Integrity**: The "health" of the agent, reduced by collisions (bruising), eating poison, and using its sensors and effectors (wear and tear)
* **Engagement**: How much the agent is engaging its environment, both by making sense of it and by acting in it

In additions to maintaining current measures of wellbeing, a CA also keeps track of the rising and falling of these measures. A sharply falling, yet still high, measure of a CA's wellbeing can be as "alarming" as a very low measure.

The wellbeing measures of a CA grow and decrease based on actions they take, bumps they suffer, food or poison they "ingest" etc. They also change from CAs sharing their individual wellbeings as "wellbeing tokens" diffuse across the collective of CAs.

## The role of wellbeing

Wellbeing provides the means by which *normativity* is associated with the beliefs of CAs. CAs correlate synchronous wellbeing levels/trends with the beliefs they synthesize from current and past observations.

Beliefs associated with consistently high or increasing wellbeing measures, are "pleasant" beliefs. Beliefs associated with consistently low or decreasing wellbeing measures are "unpleasant". Beliefs associated with neither are "neutral". Low and decreasing measures feel the worst whereas high and increasing measures feel the best.

Wellbeing drives attention: CAs intend actions to persist pleasant beliefs and terminate unpleasant beliefs. Neutral beliefs are normally "left alone" by the CA but are kept as they may compose the non-neutral beliefs of more abstract CAs.

Wellbeing also provides the motivation for CAs to spawn new CAs or to remove themselves from the SOM, so as to manage overall energy expenditure or nudge up overall engagement.

### Wellbeing and stress

Stress on a CA is caused by it having low or dropping wellbeing measures.

Stress makes a CA more *plastic*. When stressed, it is more likely to:

* revise the causal theory it uses as a symbolic generative model
* temporarily ignore acquired policy habits
* temporarily ignore strongly held beliefs and act instead on other beliefs
* lower its threshold for action
* trigger its mitosis (birthing a new CA) or apoptosis (removing itself from the SOM)

## Measures of wellbeing

### Fullness

Fullness represents the energy budget of a CA. It starts full.

An agent's collective of CAs is mortal. When there is no energy left, its mind dies (its Lego body is comparatively permanent).

Energy is replenished by the action of `eating` but only when the agent is positioned over food or poison (the agent may or may not know it is over food vs poison).

Energy is spent individually by each CA when

* obtaining a causal theory (the more time spent searching and the more complex the theory, the higher the energy cost)
* synthesizing a belief (each belief comes at a metabolic cost)
* using a causal theory (the more complex the theory, the higher the cost per use)
* remembering past observations and beliefs (additional cost per remembered observation/belief)
* completing a timeframe (baseline computational/metabolic cost)

Energy is also spent whenever the agent progressively and automatically recovers from lost integrity, i.e. repairs itself.

In response to low and/or decreasing fullness,

A CA may reduce "metabolic costs" by:

* forgetting a past state (oldest first)
* forgetting a belief ignored by all parent CAs (neutral first)
* raising the normative threshold for acting on beliefs (don't waste energy on trivial matters!)

### Integrity

Integrity represents the health of the CA. Integrity is initially full.

Integrity decreases slowly with the activation of sensors and motors (wear and tear).

Integrity is reduced more quickly whenever

* the agent's touch sensor is activated, or
* the agent executes the action of `eating` over poison food (the agent may not know to distinguish perceptually between non-food, food and poison but its "metabolism" does).

Lost integrity is recovered over time but at an energy cost proportional to the amount of recovery.

### Engagement

Engagement keeps track of how engaged a CA is. Engagement is initially empty.

Engagement goes up for a CA whenever

* it obtains an accurate enough causal theory (making sense of its umwelt),
* one of its beliefs is used in the synthesis of another CA's belief (it becomes relevant),
* whenever an action it intends is executed (it acts in the world).

Engagement decreases whenever

* a CA's belief loses relevance (it was the basis of another CA's belief that was removed), or
* slowly, with the passing of time

## Spreading wellbeing

The wellbeing of cognition actors (CAs) diffuse throughout the society of mind (SOM) as if by osmosis.

Wellbeing signals are realized by wellbeing tokens, created and destroyed, that travel between CAs without provenance info ("Your wellbeing is my wellbeing, to a point".)

The tokens diffuse down gradients up and down umwelt relationships, that is bteween CAs and their umwelts.

Within a timeframe, a CA consumes or produces wellbeing tokens depending on its activies (e.g. turning a wheel, getting a new causal theory), happenings (e.g. touch sensor bumped) and the passage of time. At the end of a timeframe, some of the tokens diffuse, by type, down to umwelt CAs and or up to parent CAs to equilibrate (down a gradient).

Once a CA has equilibrated its wellbeing tokens with its entourage (i.e. parents and umwelt), it sums up the wellbeing tokens it holds to compute its wellbeing measures by type. It keeps a snapshot in its timeframe history, enabling it to determine its wellbeing trends.

### Modulating the sharing of wellbeing

A CA can modulate the wellbeing of its umwelt by temporarily misrepresenting to its umwelt (and only its umwelt) the number of wellbeing tokens it holds .

A CA can do so by claiming to all its umwelt CAs that:

* it has fewer tokens of a given type than it really does, thus acting as a hoarder, taking up to half the pretended difference in tokens from each umwelt CA at the end of each timeframe, until it has its full
* it has more tokens of a given type than it really does, thus acting as a benefactor, sending up to half the pretended difference in tokens from each umwelt CA at the end of each timeframe, until it has none
* it has the the amount of tokens of a given type it actually does, thus either giving nor accepting tokens from its umwelt to reach equilibrium

Any CA with can change its wellbeing representation toward its umwelt. It is an action the CA can take to impact the normativity of beliefs it and its umwelt hold.

The actions are:

* hoard(wellbeing_type) -- the CA pretends to its umwelt that it has fewer wellbeing tokens of the given type (until it is full)
* donate(wellbeing_type) -- the CA pretends to its umwelt it has more wellbeing tokens of a given type (until it is empty)
* equilibrate(wellbeing type) -- the CA represents truthfully to its umwelt the number of tokens of a given type it holds

 The change in a CA's "wellbeing osmotic state" persists through the next timeframe until the next wellbeing action is taken. A CA starts life with the default stance which is to equilibrate its fullness, integrity and engagement wellbeing tokens.
