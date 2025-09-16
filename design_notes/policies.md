# Policies

A Cognition Actor (CA) seeks, through the execution of policies, to persist pleasant beliefs it holds and to terminate its unpleasant beliefs.

## Recap

A CA is part of a hierarchichal collective of CAs that animate an agent. Each CA has an umwelt composed of a small number of CAs from the (abstraction) layer below.

A CA synthesizes its beliefs from its observations, past and current, of the beliefs in its umwelt. It observes by predicting umwelt beliefs and receiving prediction errors when the predictions are wrong.

The beliefs of a CA exist in the context of wellbeing measures, current and trending. The wellbeing measures are fullness (energy), integrity (health) and engagement (relevance). They signal risks, present or absent, growing, steady or decreasing, to the survivability of a CA and, possibly and transitively, the entire collective of CAs.

Beliefs associated with high or growing risks are unpleasant. Beliefs associated with low or decreasing risks are pleasant. Others are neutral. A CA acts on its umwelt in response to the pleasantness or unpleasantness of its current beliefs.

A CA operates one timeframe after another. Each timeframe corresponds to a "thick now". The timeframe of a CA starts and stops independently of other CAs; timeframes are not synchronized. CAs higher up in the collective's hierarchy have qualitatively longer timeframes.

During its current timeframe, a CA observes the latest beliefs in its umwelt (via predictions made and prediction errors received), reads the wellbeing measures "diffused" by other CAs, refreshes its set of beliefs by integrating its latest observations with past ones, and assigns up-to-date normative values (pleasantness/unpleasantness) to its updated beliefs.

At the end of the current timeframe, a CA decides whether to act on updated beliefs and, if so, which ones, to what effect, and how.

## Intents

A CA *intends* to take action to impact its beliefs; an intent is not guaranteed to be realized. After all, a CA participates in a collective and there is only one body that the collective animates. Simultaneous intents to alter beliefs coming from multiple CAs must be resolved so that only courses of action with the highest priority are carried out by the agent at any time.

An intent by a CA consists of

* a goal - a belief held by the CA and a desired impact on it, i.e. the persisting of a pleasant belief, or the termination of an unpleasant belief
* a priority - determined by the graded normativity of the belief targeted by the intent
* a policy - how to achieve the goal by impacting (initiating, persisting, terminating) the observed beliefs held by the umwelt CAs from which the targeted CA's belief was synthesized

A CA's policy is a list of directives, to be communicated to the umwelt CAs, to achieve the CA's goal. 

A **directive** is a delegated, goal (a belief of umwelt CAs to impact) to be achieved by the umwelt *however it chooses*.

The priority of a policy reflects how unpleasant/pleasant the belief to impact is. Generally a directive from a high-level CA will have greater priority than that of a lower-level CA, but not always; low level CAs facing an "emergency" can override the policies of higher-level CAs.

The policy's directives are communicated all at once by the CA to its umwelt at the end of the CA's current timeframe. Keep in mind that, at any point in time, multiple CAs may be intending to act.

## Attention and action thresholds

The first step by a CA when preparing to act is to identify a belief to attend to, even if a parent CA has already directed the CA to impact some of its own choosing.

Only abstract (composite) beliefs can be acted on and impacted, namely `count`, `more`, `trend` and `coincide`. Concrete beliefs, those from sensor and effector CAs, and those imagined by a causal theory, represent "givens" that can not be changed though actions.

Which actionable belief is identified depends on its pleasantness/unpleasantness and whether or not it is *sufficiently* pleasant or unpleasant (activation threshold) for the CA to pay attention to it. The activation threshold is set by the current wellbeing of the CA which propagates "osmotically" throughout the entire collective.

In a low fullness context (depleted energy stores), a CA raises the threshold for action (conserve energy!), whereas, when energy is plentiful and agent engagement is low, a CA lowers the threshold for action (try something, anything!). Only a belief with normativity (pleasantness/unpleasantness) above the dynamic threshold is attended to and deemed worthy of action.

The normativity of a belief is set as a combination of absolute wellbeing values and their gradient. A positive wellbeing value is pleasant unless it is falling sharply; then it's unpleasant. Similarly, a negative wellbeing value is unpleasant unless it is rising sharply; then it's pleasant.

The CA selects which belief, if any, is *most worthy* of action in the current timeframe. Invalidating an unpleasant belief it cares about takes precedence over validating a pleasant belief. Typically, the CA will intend to terminate the most unpleasant, action-worthy belief. Else it will intend to persist the most pleasant, action-worthy belief, or iy may do something random (babble) if there is no action-worthy belief and fullness is high and steady/rising.

## Constructing a policy

A CA builds a policy when it has identified a belief it holds that need impacting, or when it receives a higher priority policy (a set of directives) from a parent CA. When receiving directives "from above", it determines which goals are relevant to it; the others are likely relevant to sibling CAs participating in the same umwelt.

Goals name umwelt beliefs and the desired impacts (initiate, persist or terminate). It is *entirely* up to the goal-receiving umwelt CA to construct a policy for the beliefs it wants to or has been requested to impact.

Once a CA has identified (or been told by a parent CA of) a belief to initiate, persist or terminate, the CA must determine its own policy to achieve this goal. The composition of the policy depends on the type of belief and on the desired impact (initiate/persist/terminate). The policy's priority depends on the CA's wellbeing (value and gradient) if originating with the CA, or on the priority of the received directive.

How to impact a belief depends on how it was arrived at. A constructed (aka abstract) belief is composed of observations (its base of support) which are themselves beliefs once or currently held in the CA's umwelt. To impact a belief a CA holds, the CA needs to impact supporting beliefs held in its umwelt.

A CA always owns a causal theory. At first, it is a trivial one that predicts what it already observed ("it is what it is"), or predicts randomly if it has yet to make observations. At some point, the CA ask sthe Apperception Engine for a causal theory informed by its history of observations of its umwelt.

The CA can use its causal theory to predict changes to the beliefs of its umwelt (i.e. incoming observations) as a result of realizing directives. This can be put to use when constructing a policy.

A causal theory has three kinds of rules

* Constraints: What is expected *never* to be observed simultaneously - e.g. not (A and B) now
* Static rules: What is expected to *always* be observed simultaneoulsy - e.g. if A and B and then also C now
* Causal rules: What is expected to be observed *next* given what was observed previously - e.g. A and B then C next

An additional but implied rule is that a previous observation survives as a current observation if it does not contradict any constraint or static rule.

A trivial causal theory has empty sets of all three kinds of rules, yielding a trivial "it is what it is" causal theory.

A CA's abstract belief integrates multiple observations (predicted beliefs in the CA's umwelt), either within the bounds of the current timeframe (`count`, `more` and `coincide` beliefs)
or of past *and* current timeframes (`trend` beliefs).

The observed umwelt beliefs involved in the composition of an abstract belief constitute the base of support of that belief. To impact an abstract belief it holds, a CA directs its umwelt to impact beliefs from which the held belief is derived and perhaps also to initiate new beliefs.

Since observations by the CA are beliefs held in the umwelt of the CA, one can see how acting becomes a recursive operation that will unfold across multiple layers of CAs and over multiple CA timeframes, until effector CAs (on the lowest level of the hierarchy of CAs) become involved and the agent's relationship with its environment is modified by running mototrs etc.

The task of constructing a policy -in order to impact a belief held by the CA- consists in deciding which supporting and observed umwelt beliefs to impact and how.

There will likely be different combinations of supporting beliefs that could be impacted and thus there could be many alternate policies to choose from.

The causal theory, a model of the generative processes causing these observations, informs the CA in the construction of hopefully effective policies by anticipating their consequences.

To recap, the CA can seek to impact a belief it holds by impacting supporting beliefs held in its umwelt.
This is achieved indirectly by the CA directing its umwelt to find a way to impact these supporting beliefs in prescribed ways (initiate vs persist vs terminate).

The only types of beliefs that can be impacted are `count`, `more`, `coincide`, and `trend` beliefs.
Concrete beliefs -sensing, action taken or imagined- can not be impacted; they are givens.

A sensing belief (e.g. distance(ir_sensor_1, 10)) is a record of a sensor reading already taken. There is no point denying it. The same applies to action beliefs (e.g. spin(motor_1, true)). There is also no point in denying it happened. An imagined belief is one abduced by the Apperception Engine to unify a causal theory. It must be accepted for as long as the causal theory is being used.

Since abstract beliefs are composed of beliefs observed in the umwelt which can themselves be abstract beliefs, a policy might be realized by more (lower-level) policies and so on until we reach only goals that can be directly impacted by activating effectors.

A CA seeking to impact an umwelt belief supporting a belief it holds can do so *directly* or *indirectly*.

### Directly impacting a belief

How a CA might **directly** impact a held belief is modulated by the kind of belief it is.

#### Impacting a `count` belief

A `count` belief encapsulates how many of a given kind of beliefs observed in its umwelt there are (for e.g., this motor was spun once).

To persist a count belief, a CA's policy would direct its umwelt CAs to persist *all of* the counted (observed) beliefs.

To initiate or terminate a count belief, a CA's policy would direct its umwelt CAs to to add a counted belief or terminate *any of* the counted beliefs.

#### Impacting a more belief

A `more` belief expresses that there is more of than another in its umwelt.

To initiate or teminate a more belief, a CA's policy would direct its umwelt to initiate or to terminate a compared, count belief.

To persist a more belief, a CA's policy would direct its umwelt CAs to persist both compared counts.

#### Impacting a coincide belief

A `coincide` belief captures the fact that two or more umwelt beliefs are consistently observed together.

A coincide belief can be intentionally initiated by initiating all missing co-occuring umwelt beliefs.

A coincide belief be persisted by persisting all the co-occuring umwelt beliefs.

A coincide belief be terminated by terminating any of the co-occuring umwelt beliefs.

#### Impacting a trend belief

A `trend` belief captures how a given kind of observed belief is changing across the latest timeframes of the CA, for example, "distance keeps diminishing" is a "down" trend.

To initiate a trend belief, a CA policy could change the ordinal value of the trending umwelt belief.
To persist a trend belief, a CA's policy would direct its umwelt to **further** the trend.
To terminate a trend belief, a CA's policy would direct its umwelt to **disrupt** the trend.

How a trend belief is impacted depends on the assigned value of the trend (up or down).

An `up` trend captures an upwardly changing ordinal value for a given property of a given object.
A `down` trend captures a downwardly changing ordinal value for a given property of a given object.

If the nature of the trend to impact is

* up
  * to disrupt it, reduce or stabilize the values of the observed, trending belief
  * to further it, increase the values of the observed, trending belief
* down
  * to disrupt it, increase or stabilize the values of the observed, trending belief
  * to further it, decrease the values of the observed, trending belief

### Indirectly impacting a belief given a causal theory

A CA can impact a belief A **indirectly** by impacting a *causally linked*, observed belief B.

* if A and B are mutually exclusive (according to the CA's causal theory) then
  * initiating B should terminate A
  * persisting B should prevent A
  * terminating B should allow for A
* if A and B must co-exist under some condition then
  * initiating B should initiate A
  * persisting B should persist A
  * terminating B should terminate A
* if B causes A under some condition then
  * initiating B should eventually initiate A
  * persisting B should persist or eventually initiate A
  * terminating B *might* terminate A

## Executing a policy

A policy is a set of directives to be realized by a CA's umwelt in order to impact a belief held by the parent CA.

A directive is a prioritized goal meant by the CA for its umwelt, a goal being an observed belief plus its desired initiation, continuation or termination (the umwelt is free to formulate an appropriate policy).

If the the CA is an *effector CA*, the goals it receives will simply be to activate effectors, like spinning a wheel forward or backward a number of times. Effector CAs are at the bottom level of the hierarchy of CAs and are indirectly and transitively in the umwelts of every CAs. A policy is thus ultimately realized via cumulated actions taken by effector CAs.

A CA executes a policy it formulates or has received at the close of its current timeframe, once it has made new observations and updated its beliefs from them.

### Observing action beliefs from executed policies

When a CA executes a policy it formulated, the execution of the policy possibly becomes a set of `Action(Effector, Boolean)` beliefs (a.k.a. action beliefs) held by effector CAs sitting at the bottom of the CA hierarchy.

These action beliefs held by effector CAs are automatically elevated up the hierarchy, becoming beliefs shared by ancestor CAs, subject to consistency constraints (no disagreement among siblings) and abstraction constraints (they are not combined into abstract beliefs).

Crucially, the action beliefs from the execution of the policy, like any other umwelt beliefs observed by a CA, can become incorporated into the CA's causal theory when it is updated.

### Evaluating the success of reusable policies

The CA remembers, for a while, a policy it executed (the goal -the belief to impact- and the directives emitted) together with the wellbeing values at the time, so as to later be able to gauge the success of the policy.

A policy is deemed successful if it precedes closely the intended belief change. It is even more successful if it correlates with an increase in wellbeing.

A CA might repeat a past policy considered the most successful in attempting to achieve a goal, or it might try another pre-built policy, or it might even construct a new one, all depending on the stress felt by the CA from changes in its wellbeing.

### Execution protocole

* CAs may receive intent events during their open timeframes (intents received when a timeframe is closed but not ended are accumulated and given to the next timeframe when it opens)
* At the close of its timeframe, a CA produces its own self-serving goals, prioritize them and compare priorities with the received intents
* A CA selects either a received intent it can help realize, or a self-assigned goal it intends to realize
  * The CA allocates an amount to time in which to try to realize the received intent or the self-assigned goal
  * If a self-assigned goal is selected
    * The CA builds/reuses a policy to realize it and emits an intent with the policy directives and a priority
    * It messages the parents that sent intents that the intended goals can not be actuated
  * If a received intent is selected
    * For each goal matching a belief it holds
      * It builds/reuses a policy and emits an intent
    * The child CA tells the intending parent CA that what goals it can actuate
* When the intending CA hears from all child CAs about all actualizable goals in the intent it emitted
  * If any intended goal can not be actuated by any child CA, then the intent can not be realized
    * The CA emits that the intent completed in failure
    * The CA looks for an alternative policy unless time allotted is expired
  * If all intended goals can be actuated
    * For each such goal
      * The CA select one child CA who can actuate and tells it to ready actuation
        * It tells the others not to actuate
    * Once all selected CAs have reported that they have readied actuation
      * If the CA originated the intent from a self-selected goal, it tells the body to execute readied actuations
      * Else if the intent was to realize a received goal (as a directive in an intent from a parent CA)
        * Tell the parent CA that the received intent's goal actuation is readied

### Actuation flow

Let's assume:

* CA_3 is in the umwelt of CA_2.
* CA_2 and CA_2s are in the umwelt of CA_1.

```mermaid
---
title: UMWELTS (ER diagram)
---
erDiagram
CA_1 {
  type dynamic
}
CA_2 {
  type dynamic
}
CA_2s {
  type effector
}
CA_3 {
  type effector
}

 CA_1 ||--|| CA_2 : has_child
 CA_1 ||--|| CA_2s : has_child
 CA_2 ||--|| CA_3 : has_child
 CA_2s ||..|| Body : actuates
 CA_3 ||..|| Body : actuates
```

```mermaid
---
title: ACTUATING (sequence diagram) 
---
sequenceDiagram;
  participant CA_1
  participant CA_2
  participant CA_2s
  participant CA_3
  participant Body
  CA_1-)CA_2: intent(id1, priority, [goal1.1, goal1.2...])
  CA_1-)CA_2s: intent(id1, priority, [goal1.1, goal1.2...])
  CA_2-)CA_3: goal1.1:intent(id2, priority, [goal2.1,goal2.2...])
  CA_3->>CA_2: can actuate([goal2.1, goal2.2])
  CA_2->>CA_1: can actuate([goal1.1])
  CA_2s->>CA_1: can actuate([goal1.1, goal1.2])
  CA_2s->>CA_2s: terminate timeframe

  CA_1->>CA_2s: ready_actuation(goal1.1, false)
  CA_1->>CA_2: ready_actuation(goal1.1, true)
  CA_2->>CA_3: ready_actuation(goal2.1, true)
  CA_2->>CA_3: ready_actuation(goal2.2, true)
  CA_3->>Body: actuate effector
  CA_3->>CA_2: actuation_ready(goal2.1)
  CA_3->>CA_2: actuation_ready(goal2.2)
  CA_2->>CA_1: actuation_ready(goal1.1)
  CA_1->>CA_2s: ready_actuation(goal1.2, true)
  CA_2s->>Body: actuate effector
  CA_2s->>CA_1: actuation_ready(goal1.2)

  CA_1-->>Body: execute
  CA_2-)CA_3: intent completed(id2, true)
  CA_2->>CA_2: terminate timeframe
  CA_1-)CA_2s: intent completed(id1, true)
  CA_1-)CA_2: intent completed(id1, true)
  CA_1->>CA_1: terminate timeframe
```

### Timeframe termination

* If a CA emits an intent, it terminates its timeframe once its intent is completed.
* A CA that received an intent but did not emit one, terminates its timeframe once it confirmed which goals it could actuate.
  * The potential actuations are retained into the new timeframe awaiting readying requests.
    * It is possible that, by the time, a CA receives a readying request, its beliefs have shifted and the actuation is obsolete.
    * This is disregarded and the actuation is nonetheless readied.
* A CA that did not receive an intent nor emitted one terminates its current timeframe immediately.
