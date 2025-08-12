# Cognition actors

A CA strives to become increasingly compentent at making sense of its umwelt and at honing its beliefs through actions.

A CA makes sense of its umwelt (a few lower-level CAs) by predicting changes to it (i.e. predicting incoming observations of its umwelt CAs' beliefs)
and by deriving its own beliefs from trends in past observations that then become observations available to parent CAs (higher-level CAs that have the CA in their umwelts).

A CA is effective at impacting its umwelt if it has reliable policies it can apply to validate pleasant beliefs or invalidate unpleasant beliefs.
A belief is pleasant if it was derived in the context of improving wellbeing, unpleasant in the context of worsening wellbeing

The more competent a CA is, the more likely it is that its parents CAs will be competent and survive, and thus the more likely it is that the CA itself will survive; orphaned CAs are susceptible to being removed when wellbeing is low.

## Timeframe and memory

A CA operates one timeframe after another. The current timeframe of a CA corresponds to a "thick now"; all observations made and all beliefs updated by the CA during this timeframe are considered synchronous. Timeframes are not synchronized across CAs. The timeframe of a CA starts and stops independently of those of other CAs. The current timeframes of CAs partially and randomly overlap.

During its current timeframe, a CA makes new observations by predicting the latest beliefs of CAs in its umwelt, update its wellbeing measures, refresh its set of beliefs by integrating the latest observations with past ones, and assign up-to-date normative values (pleasantness/unpleasantness) to its updated beliefs.

At the end of the current timeframe, a CA decides whether to act on its updated beliefs and, if so, how.

Upon completing its current timeframe, a CA adds the state of the timeframe to its memory of past states. The CA uses its remembered past states to compute its wellbeing gradients, derive its current (pleasant vs unpleasant) beliefs, and update the causal theory that explains its past observations and predicts its incoming observations.

CAs higher up in the collective's hierarchy have longer timeframes and longer memories (more states are remembered). When the maximum number of remembered states is reached and the latest state is committed to memory (upon completion of the current timeframe), the oldest state is dropped from memory.

There is a "metabolic" cost associated with memory. The higher a CA's metabolic costs, the faster its fullness wellbeing drains. A CA under stress from low fullness might reduce the size of its memory to reduce this drain. Regaining high fullness would restore the prior bound on the CA's memory size.

## Observing (its umwelt's beliefs)

* A CA predicts its observations of the beliefs of CAs in its umwelt
  * If the CA has no prior observations, it makes random, domain-bounded predictions about all beliefs in its umwelt
  * If the CA has no causal theory but has prior observations, it predicts that the latest observations are unchanged.
  * If the CA has a causal theory, it uses it to predict the next observations.
* A CA predicts the success of its policies since an executed policy is also an observation
* If a prediction is met with a prediction error, the prediction error becomes the latest observation, else the uncontested prediction is the observation.
* A CA drops repeated states (state = observations in the same timeframe) - i.e. a CA's perceived time stands still while its umwelt does not appear to change

## Understanding (relating observations causally and via constraints)

* To be competent, a CA needs to make sense of its observations via a causal theory of
  * how its umwelt changes on its own
  * how its umwelt changes from executed policies
* A CA requests a causal theory from the Apperception Engine when
  * it has no theory and a theory could be generated from its remembered states
  * it has a theory and its predictive capabilities have degraded since acquired such that it is no longer good enough
  * it has a theory but has had policies executed since the theory was generated
* A CA's causal theory integrates beliefs across its umwelt
  * necessary co-occurrences of observations from static rules
    * if a static rule states "A whenever B and C:, then observing B and C at time T infers (deductively) observing A also at T
    * e.g if the proximity got smaller then the ambient light must also have gotten brighter
  * sequencing of observations from causal rules
    * if a causal rule states "A after B and C", then
      * observing A at time T entails (abductively) B and C at T-1
      * having observed B and C at T-1 entails (deductively) A at time T
    * e.g. the color becomes gray if the color was green
* Inferred observations (that are not also umwelt-affirmed observations) are marked as "inferred" to distinguish them
  * A new causal theory leads the CA to reconsider inferred observations across remembered states (i.e. it is revising some of its observed past)
  * A CA reconsidering its past is opaque to parent CAs
    * A CA never questions observations affirmed by its umwelt (even if umwelt CAs might reconsider their past affirmed beliefs)
      * Because the internal belief state of a CA is opaque to other CAs and is only revealed by
        * prediction errors
        * and events signaling new belief predicates (names and domains) and new (latent) objects
          * affording new kinds of predictions
* The CA applies the theory's causal rules to predict the next state so it can make predictions
  * from the execution of a policy selected to achieve an intent (impacting a held belief)
  * due to "spontaneous" changes in the umwelt
* The parent CAs constrain the vocabulary of a CA's causal theory (how the CA can express a symbolic generative model), should the CA look for a better one
  * or else beliefs of parent CAs based on latent observations would become unfounded
  * the parent CAs can provide these constraints to the CA
* Up-down and down-up constraints
  * Parent CAs constrain the space of causal theories of the CAs in their umwelts
    * By constraining their vocabularies
  * Umwelt CAs constrain the space of beliefs of their parent CAs
    * By constraining what the parent CAs' beliefs can be derived from

## Believing (detecting patterns of change in observations)

* A sensor CA has atomic beliefs obtained from Kalman-filtered measurements
* A non-sensor CA gets its beliefs
  * from the objects and relations/properties abduced by its causal theory
  * from the facts of having executed policies
  * from detecting patterns in the current and remembered observations of its umwelt
    * patterns such as counts, endings, comparisons and trends
      * these beliefs are not be inferrable from the causal theory (state-to-state transitions)
      * e.g. the distance getting smaller is stable (trend about a trend)
* See [beliefs.md](./beliefs.md)
* A CA has no belief until it abduces objects/relations/properties, executes policies or detects patterns
* Naming a synthetic belief (a synthetic belief is one the CA derived from detecting a pattern in its obeservations or from the execution of a policy it defined)
  * The CA assigns an agent-wide, forever unique predicate name to the belief
  * The CA remembers and hides the derivation of the belief (a synthetic belief is opaque)
* A CA's belief domain grows when
  * a new observation pattern (whatever its value) is detected and named
    * changing the *value* of a belief does not add to the *domain* of beliefs the CA makes available as observations to parent CAs
* Exposing a synthetic belief
  * A CA exposes its belief domain (names of its beliefs) in a manner indistinguisable from atomic properties or relations
* Beliefs are (if transitively opened up) recursive structures (trends of trends ... of atomic properties/relations)
  * They are composed of simpler beliefs, down to atomic beliefs (held by sensor CAs)
  * This makes beliefs potentially semantically transparent to an outside observer but obscure between CAs

## Acting (on beliefs)

* A CA seeks to validate a pleasant belief and invalidate an unplesant belief
  * By furthering or interrupting (i.e. impacting) sub-beliefs via intents delegated to umwelt CAs
* Realizing an intent is recursive because a belief is a recursive structure of beliefs held by umwelt CAs
* See [policies.md](./policies.md)
* A CA receiving a directive (a prioritized goal to achieve, i.e. a belief to initiate/persist/terminate with some degree of urgency) from a parent CA will, depending on accepting the directive,
  * construct/reuse a policy to achieve the received goal
    * based on its causal theory which might describe alternate causes for the same outcome
    * or on guesses if it has no theory yet (babbling)
* One policy execution at a time
  * A CA can not intend to realize one of its own goal if it is executing a parent CA's policy
    * Lower-level CAs relinquish some autonomy for the greater good
* Learning affordances
  * A CA gets feedback as to whether the intents in an executed policy were realized
  * A CA remembers how successul each policy was at achieving a goal
    * A CA selects the more recently successful policies more often (it will also sometimes try others in case they might be better)
  * A CA can randomly construct a policy to observe what happens if executed (it babbles)
    * when given the opportunity
      * all wellbeing levels are high and the CA is not involved in a parent's intent
    * or when necessary
      * the CA lacks beliefs (because the umwelt does not change) and thus has no affordances

## Attention

* A belief, when synthesized, is associated with a wellbeing/pleasantness trend (better, worse, same)
  * A CA remembers the ambient wellbeing at each timeframe
* A CA normally does not intend to further/disrupt beliefs when wellbeing trends not far enough from neutral
* Higher-level beliefs are more likely to be associated with clear wellbeing trends than lower-level beliefs
  * This drives the SOM to add levels until clear wellbeing trends appear
  * Afforded control over wellbeing makes up for the higher resource consumption of added SOM levels

## Responding to wellbeing measures

* A CA updates its wellbeing measures (fullness, integrity and engagement).
  * It starts life with highest fullness, highest integrity and lowest engagement (all initially broadcasted)
* See [wellbeing.md](./wellbeing.md)
* CAs signal their changing wellbeing to other CAs
* In each timeframe, a CA may respond to the latest brodacasted measures by operating on its internal data
* It responds to
  * low fullness by
    * getting rid of an ineffective policy (if any)
    * else getting rid of an irrelevant belief (if any)
    * else forgetting the oldest state (unless it supports held beliefs)
  * high fullness by
    * trying to upgrade the causal theory
  * low integrity by
    * ratcheting up pleasantness threshold for triggering intents (reduces likelihood to act)
  * high integrity or low engagement
    * ratcheting down pleasantness threshold for triggering intents (increases likelihood to act)
      * When threshold is 0, attempts will be made to impact even neutral beliefs
  * high fullness and high integrity
    * babbling: goal-free intents are emitted to "see what happens"
