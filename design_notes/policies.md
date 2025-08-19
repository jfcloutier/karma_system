# Policies

A Cognition Actor (CA) seeks to persist pleasant beliefs it holds and to terminate its unpleasant beliefs through the execution of policies.

## Recap

A CA is part of a hierarchichal collective of CAs that animate an agent. Each CA has an umwelt composed of a small number of CAs from the (abstraction) level below.

A CA synthesizes its beliefs from its observations, past and current, of the beliefs in its umwelt. It observes by predicting these beliefs and receiving prediction errors when the predictions are wrong.

The beliefs of a CA exist in the context of wellbeing measures, current and trending. The wellbeing measures are fullness, integrity and engagement. They signal risks, present or absent, growing, steady or decreasing, to the survivability of a CA and, possibly, the entire collective of CAs.

Beliefs associated with high or growing risks are unpleasant. Beliefs associated with low or decreasing risks are pleasant. Others are neutral. A CA acts on its umwelt in response to the pleasantness or unpleasantness of its current beliefs.

A CA operates one timeframe after another. Each timeframe corresponds to a "thick now". The timeframe of a CA starts and stops independently of other CAs; timeframes are not synchronized. CAs higher up in the collective's hierarchy have qualitatively longer timeframes.

During its current timeframe, a CA observes the latest beliefs in its umwelt (via predictions and prediction errors), reads the wellbeing measures "diffused" by other CAs, refreshes its set of beliefs by integrating its latest observations with past ones, and assigns up-to-date normative values (pleasantness/unpleasantness) to its updated beliefs.

At the end of the current timeframe, a CA decides whether to act on updated beliefs and, if so, which ones, to what effect, and how.

## Intents

A CA at most *intends* to take action to impact its beliefs; an intent is not guaranteed to be realized. After all, a CA participates in a collective and there is only one body that the collective animates. Simultaneous intents to alter beliefs coming from multiple CAs must be resolved so that only courses of action
with the highest priority are carried out by the agent at any time.

An intent by a CA consists of

* a goal - a belief held by the CA and a desired impact on it, i.e. the persisting of a pleasant belief, or the termination of an unpleasant belief
* a priority - determined by the graded normativity of the belief targeted by the intent
* a policy - how to achieve the goal by impacting (initiating, persisting, terminating) the observed beliefs held by the umwelt CAs from which the targeted CA's belief was synthesized

A policy is a list of directives, to be communicated to the umwelt CAs. A directive is a delegated, prioritized goal (a belief of umwelt CAs to impact) to be achieved by the umwelt *however it chooses*.

The priority combines the level of the emitting CA with a number proportional to how unpleasant/pleasant the belief to impact is. Generally a directive from a high-level CA will have greater priority than that of a lower-level CA, but not always; low level CAs facing an "emergency" can override higher-level CAs in having their policies take precedence.

The policy's directives are communicated all at once by the CA to its umwelt at the end of the CA's current timeframe. Keep in mind that, at any point in time, multiple CAs may be intending to act.

## Attention and action thresholds

The first step by a CA when preparing to act is to identify a belief to attend to, even if a parent CA has already directed the CA to impact some of its own choosing.

Only abstract (composite) beliefs can be acted on and impacted, namely `count`, `more`, `trend`, `coincidence` and `ended`. Concrete beliefs, those from sensor and effector CAs, and those imagined by a causal theory, represent "givens" that can not be changed though actions.

Which actionable belief is identified depends on its pleasantness/unpleasantness and whether or not it is *sufficiently* pleasant or unpleasant (activation threshold) for the CA to pay attention to it. The activation threshold is set by the current wellbeing of the CA which propagates "osmotically" throughout the entire collective.

In a low fullness context (depleted energy stores), a CA raises the threshold for action (conserve energy!), whereas, when energy is plentiful and agent engagement is low, a CA lowers the threshold for action (try something, anything!). Only a belief with normativity (pleasantness/unpleasantness) above the dynamic threshold is deemed worthy of action.

The normativity of a belief is set as a combination of absolute wellbeing values and their gradient. A positive wellbeing value is pleasant unless it is falling sharply; then it's unpleasant. Similarly, a negative wellbeing value is unpleasant unless it is rising sharply; then it's pleasant.

The CA selects which belief, if any, is *most worthy* of action in the current timeframe. Invalidating an unpleasant belief it cares about takes precedence over validating a pleasant belief. Typically, the CA will intend to terminate the most unpleasant, action-worthy belief. Else it will intend to persist the most pleasant, action-worthy belief, or iy may do something random (babble) if there is no action-worthy belief and fullness is high and steady/rising.

## Constructing a policy

A CA builds a policy when it has identified a belief it holds that need impacting, or when it receives a higher priority policy (a set of directives) from a parent CA. When receiving a policy, it determines which goals are relevant to it; the others are likely relevant to sibling CAs participating in the same umwelt.

Goals named beliefs (the objects of abstract beliefs the named beliefs compose) and the desired impacts. It is *entirely* up to the goal-receiving CA to construct a policy for the beliefs it wants to or has been requested to impact.

Once a CA has identified (or been told by a parent CA of) a belief to initiate, persist or terminate, the CA must determine a policy to achieve this goal. The composition of the policy depends on the type of belief and on the desired impact (initiate/persist/terminate). The policy's priority depends on the CA's wellbeing (value and gradient) if originating with the CA, or on the priority of the received directive it realizes if the goal originates from another CA.

The type of belief and the desired impact determine the *base of support* of the belief to be impacted.
An abstract belief is composed of observations (its base of support) which are themselves beliefs once or currently held in the CA's umwelt. To impact a belief a CA holds, the CA needs to impact supporting beliefs held in its umwelt.

A CA always owns a causal theory. At first, it is an empty one that trivially predicts what it already observed ("it is what it is"), or predicts randomly if it has yet to make observations. Later the CA will ask the Apperception Engine for a new causal theory, this time informed by its history of observations of its umwelt.
The CA can use its causal theory to predict changes to the beliefs of its umwelt (i.e. incoming observations) as a result of executing particular directives. This can be put to use when constructing a policy.

A causal theory has three kinds of rules

* Constraints: What is expected *never* to be observed simultaneously - e.g. not (A and B) now
* Static rules: What is expected to *always* be observed simultaneoulsy - e.g. if A and B and then also C now
* Causal rules: What is expected to be observed *next* given what was observed previously - e.g. A and B then C next

An additional but implied rule is that a previous observation survives as a current observation if it does not contradict any constraint or static rule.

A trivial causal theory has empty sets of all three kinds of rules, yielding a trivial "it is what it is" causal theory.

A CA's abstract belief is the composition of multiple observations (of beliefs in the CA's umwelt), either within the bounds of the current timeframe (`count`, `more` and `coincidence` beliefs)
or integrating past and current timeframes (`trend` beliefs).

Remember that the observations involved in the composition of an abstract belief constitute the base of support of that belief that may be targeted for impact, and that, to impact a belief, i.e. initiate, persist or terminate it, the CA will want to impact all or some of the supporting observations, and perhaps also initiate new ones.

Since observations by the CA are beliefs held in the umwelt of the CA, one can see how acting becomes a recursive operation that will unfold across multiple layers of CAs and over multiple CA timeframes, until effector CAs (on the lowest level of the hierarchy of CAs) become involved and the agent's relationship with its environment is modified.

The task of constructing a policy -in order to impact a belief held by the CA- consists in deciding which supporting and observed umwelt beliefs to impact and how.

There will likely be many possible combinations of supporting beliefs to impact and thus there could be many alternate policies to choose from.

The causal theory, a model of the generative processes causing these observations, informs the CA in the construction of hopefully effective policies by anticipating their consequences.

To recap, the CA could impact a belief it holds by impacting supporting beliefs held in its umwelt.
This is achieved indirectly by the CA requesting its umwelt to find a way to impact these supporting beliefs in prescribed ways (initiate vs persist vs terminate).

The only types of beliefs that can be impacted are `count`, `more`, `coincidence`, and `trend` beliefs.
Concrete beliefs (sensing, action or imagined) can not be impacted; they are givens. This would be tantamount to neurosis; a belief abduced to unify a causal theory it posited as given, until a new causal theory is acquired that is without it.

A sensing belief (e.g. distance(ir_sensor_1, 10)) also can not be impacted for the same reason: It is a record of a sensor reading already taken; no point denying it. The same applies to action beliefs (e.g. spin(motor_1, true)).

Since abstract beliefs are composed of beliefs observed in the umwelt which can themselves be abstract beliefs. A policy might be realized by more (lower-level) policies and so on until we reach only goals that are concrete beliefs that can be directly impacted, namely action beliefs, by activating effectors.

Let's say a CA wants to impact an observation A that supports a belief it intends to initiate, persist or terminate. It can do so *directly* or *indirectly*.

### Directly impacting a belief

How a CA might **directly** impact a held belief is modulated by the kind of belief it is.

#### Impacting a `count` belief

A `count` belief encapsulates how many of a given kind of observed beliefs there are in the current timeframe (for e.g., this motor was spun once).

To persist a count belief, a CA's policy would direct its umwelt CAs to persist *all of* the counted (observed) beliefs.

To initiate or terminate a count belief, a CA's policy would direct its umwelt CAs to to add a counted belief or terminate *any of* the counted beliefs.

#### Impacting a more belief

A `more` belief expresses that more of an object was counted than another.

To initiate or teminate a more belief, a CA's policy would direct its umwelt belief to initiate or to terminate a compared, counted belief.

To persist a more belief, a CA's policy would direct its umwelt CAs to persist both compared counts.

#### Impacting a trend belief

A `trend` belief captures how a given kind of observed belief is changing across the latest timeframes of the CA, for example, "distance keeps diminishing" is a "down" trend.

To initiate a trend belief, a CA policy could change the ordinal value of a started belief.
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

#### Impacting a started belief

A `started` belief captures the fact that an observation not made in a previous timeframe has now been made.

A started belief can be intentionally initiated by causing pre-conditions for it (as stated by a causal theory).

A started belief, by definition, can not be persisted or terminated: it happened at a point in time and that can't be changed.

#### Impacting an ended belief

An `ended` belief captures the fact that an observation from a previous timeframe has disappeared in the current timeframe.

To initiate an ended belief is simply to terminate the belief.

An ended belief, by definition, can not be persisted or terminated: it happened at a point in time and that can't be changed.

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

## Impacting a belief by executing a policy

A policy is a set of directives to be realized by a CA's umwelt in order to impact a belief held by the parent CA.

A directive is a prioritized goal meant by the CA for its umwelt, a goal being an observed belief plus its desired initiation, continuation or termination (the umwelt is free to formulate an appropriate policy).

If the the CA is an *effector CA*, the goals it receives will simply be to activate effectors, like spinning a wheel forward or backward a number of times.
Effector CAs are at the bottom level of the hierarchy of CAs and are indirectly and transitively in the umwelts of every CAs.
A policy is thus ultimately realized via cumulated actions taken by effector CAs.

A CA executes a policy it formulates or has received at the close of its current timeframe, once it has made new observations and updated its beliefs from them.

### Protocol for executing policies

Note: The protocol implements something akin to multi-phase commits on composite transactions (only once a policy in play is recursively marked as executable is it recursively executed).

parent CA --- intent(directives) -->> umwelt CAs
parent CA <-- can_actuate(goals - can be empty) --- umwelt CA
parent CA --- ready_actuation(goal) ---> umwelt CA
...
parent CA <-- actuation_ready(goal) --- umwelt CA
...
(initiating CA tells the body to execute all primed actuations)
initiating CA ---- executed ---->> all CAs
parent CA <<-- wellbeing_changed -- umwelt CA

Note: -->> denote event broadcasts and --> denote message unicasts

### Steps

At the end of a timeframe, a CA

* selects a goal -this becomes a "self-directed" goal because it originated with the CA-
* and formulates a policy (a list of directives) to achieve the goal,
* and marks the goal as "in play",
* and broadcasts the policy *intent* to its umwelt CAs.

A CA keeps a list of the policies (as a conjunction of directives) it receives from its parents within its current timeframe.

At the end of its current timeframe, a CA:

* rejects irrelevant policies (none of the goals of the policy reference beliefs the CA holds or could hold),
* sorts the remaining policies by priority (highest first),
* selects the highest priority policy remaining, if any,
* processes these directives, if any
* notifies originating CAs of the directives from that policy it can actuate,

Note: A CA processes at most one policy at a time. A new timeframe is started only once the selected policy, if any, is rejected or executed.

A CA's timeframe must thus be qualitatively longer than that of its umwelt CAs, to the point where, to an observer, it operates on a different time scale than its umwelt.

For each goal in the retained policy directives:

* If the CA is an effector, the goal is marked as "ready to actuate" and the CA communicates to the CA of origin that the goal is "actuation-ready"
* else, for higher-level CAs, the goal is marked "in play" and the CA formulates a policy to realize it (i.e. recursively executes the steps)

The receiving CA informs the originating CA when each directive is "actuation-ready".

A CA that emitted a policy to its umwelt CAs to achieve a goal (i.e. impact a belief it holds) keeps the goal in play:

* Until **any** directive in the emitted policy is reported as rejected by **all** umwelt CAs (all umwelt CAs reporte and none can actuate the directive)
  * The CA then communicates to the originating CA that the received goal, for which the CA formulated the rejected policy, was rejected, taking the goal out of play
* Or until **all** directives in the policy are reported as actuatable by **one or more** of the umwelt CAs
  * The CA then communicates to the originating CA, if any, that the received goal, for which the CA formulated the policy, is actuable (can actuate), and moves it from in play to actuation-ready

If the "self-directed" goal is marked as "actuation-ready", the CA instructs *selected* umwelt CAs to ready actuation for each directive in the policy.
When all selected umwelt CAs report as "ready to actuate", the CA emits the "execute" event and the goal is taken out of play
If the self-directed goal's policy is rejected, the goal is taken out of play and nothing is done.

When a CA receives a message to ready actuation  of it goals in play

* If the CA is an effector CA that can actuate the goals
  * the CA instructs its body effector to prepare actuation of the action-as-goal
  * and reports it as actuation-ready to the originating CA
* Else, if not an effector CA, for each directive in the policy it formulated to achieve the received goal
  * It selects a preferred umwelt CA to ready actuation the directive (more than one umwelt CA might be ready, making the others redundant)
    * It instructs the selected umwelt CA to prepare to execute the policy it built if the directive is a goal

Once all the directives in the policy a CA emitted are reported to it as "actuation-ready" (the body is primed for actuation), execution by the body is triggered.
The goal for which the policy was formulated by the CA is then no longer active.

When all goals of a CA are inactivated (rejected or executed), a new frame is started.

## Observing executed policies as attempt beliefs

When a CA executes a policy it formulated, the execution of the policy becomes a `count(PolicyName, 1)` belief held by the CA in its next timeframe.

The belief from the execution of the policy, like any other belief of the CA, is observable by a parent CA, and, crucially, can be incorporated into the parent CA's symbolic generative model (causal theory).

The policy's contents (a list of goals for the CA's umwelt) is known to the CA but is hidden to its observers (i.e. parent CAs).

The CA remembers named policies at least for as long as parent CAs references them.
