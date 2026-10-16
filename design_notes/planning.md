# Building plans

A Cognition Actor (CA) seeks, through the execution of plans, to create pleasant percepts, persist those it already has, and terminate unpleasant ones.

## The logic of plans

A CA builds a plan when it has identified a current percept it wants to have, persist or terminate (to realize its intent), or when it receives a prediction from a parent CA about it impacting a percept it may have (to realize a parent's directive). When receiving directives (as predictions) from parents, a CA determines which received are relevant to it; the others are likely relevant to sibling CAs participating in the same umwelt.

Intents and directives are goals. Goals name umwelt percepts and the desired impacts (create, persist or terminate). It is *entirely* up to the goal-receiving umwelt CA what plan it constructs given a goal to achieve.

The composition of the plan depends on the type of percept and on the desired impact (create/persist/terminate). The plan's priority depends on the CA's feeling (wellbeing value and gradient) if originating with the CA, or on the priority of the received directive.

How to impact a percept depends on how it was arrived at. A constructed (aka synthetic) percept is composed of observations (as evidence) which are themselves umwelt percepts the CA observed. To impact a percept a CA holds, the CA needs to impact percepts it observed as held in its umwelt.

A CA may have a causal theory. At first, it has none. At some point, the CA asks the Apperception Engine for a causal theory informed by its history of observations of its umwelt.
The CA can use its causal theory to predict changes to the percepts of its umwelt (i.e. incoming observations) as a result of realizing directives. This can be put to use when constructing a plan.

A causal theory has three kinds of rules

* Constraints: What is expected *never* to be observed simultaneously - e.g. not (A and B) now
* Static rules: What is expected to *always* be observed simultaneoulsy - e.g. if A and B now and then also C now
* Causal rules: What is expected to be observed *next* given what is observed now - e.g. if A and B now then C next

An additional but implied rule is that a previous observation survives as a current observation if it does not contradict any constraint or static rule. Until it fades.

A CA's synthetic percept integrates multiple observations (predicted percepts in the CA's umwelt), either within the bounds of the current timeframe (`count`, and `more` percepts)
or of past *and* current timeframes (`trend` percepts).

The observed umwelt percepts involved in the composition of a synthetic percept constitute the evidence for that percept. To impact a synthetic percept it holds, a CA directs its umwelt to impact percepts from which the held percept is derived (its evidence) and perhaps also to create new percepts.

Since observations by the CA are percepts held in the umwelt of the CA, one can see how acting becomes a recursive operation that will unfold across multiple layers of CAs and over multiple CA timeframes, until effector CAs (on the lowest level of the hierarchy of CAs) become involved and the agent's relationship with its environment is modified by running motors etc.

The task of constructing a plan -in order to impact a percept held by the CA- consists in deciding which umwelt percepts to impact and how.

There will likely be different combinations of umwelt percepts that could be impacted and thus there could be many alternate plans to choose from.

The causal theory, a model of the generative processes causing these observations, if present, informs the CA in the construction of hopefully effective plans by inferring their consequences.

To recap, the CA can seek to impact a percept it holds, or create a new one, by impacting causative percepts held in its umwelt.
This is achieved by the CA directing its umwelt (via predictions) to find a way to impact their percepts in prescribed ways (create vs persist vs terminate).

The only types of percepts that can be impacted are `count`, `more`, and `trend` percepts. A sensing percept (e.g. distance(ir_sensor_1, 10)) is a record of a sensor reading that was taken. There is no point denying it (the CA might still want to validate it though). There is also no point in denying it happened. An imagined percept is one abduced by the Apperception Engine to unify a causal theory. It must be accepted as "real" for as long as the causal theory is used.

A CA seeking to impact an umwelt percept from which it synthesized a percept it itself holds can do so *directly* or *indirectly*.
Since synthetic percepts are composed of percepts observed in the umwelt which can themselves be synthetic percepts, a plan might be realized by more (lower-level) plans and so on until we reach only goals that can be directly impacted by activating effectors.

### Building a plan to impact a percept

How a CA might **directly** impact a held percept is modulated by the kind of percept it is.

#### Impacting a `count` percept

A `count` percept encapsulates how many of a given kind of percepts observed in its umwelt there are (for e.g., this motor was spun twice).

To persist a count percept, a CA's plan would direct its umwelt CAs to persist *all of* the counted (observed) percepts.

To create or terminate a count percept, a CA's plan would direct its umwelt CAs to add a counted percept or terminate *any of* the counted percepts.

#### Impacting a more percept

A `more` percept expresses that there is more of something than another in its umwelt.

To create or teminate a more percept, a CA's plan would direct its umwelt to create or to terminate a compared, count percept.

To persist a more percept, a CA's plan would direct its umwelt CAs to persist both compared counts. It could also create or terminate percepts in equal amounts on both sides of the ledger.

#### Impacting a trend percept

A `trend` percept captures how a given kind of observed percept is changing across the latest timeframes of the CA, for example, "distance keeps diminishing" is a "down" trend.

To create a trend percept, a CA's plan could change the ordinal value of the trending umwelt percept.
To persist a trend percept, a CA's plan would direct its umwelt to **further** the trend.
To terminate a trend percept, a CA's plan would direct its umwelt to **disrupt** the trend.

How a trend percept is impacted depends on the assigned value of the trend (up, down or steady).

An `up` trend captures an upwardly changing ordinal value for a given property of a given object.
A `down` trend captures a downwardly changing ordinal value for a given property of a given object.
A `steady` trend captures an unchanging ordinal value for a given property of a given object after it trended.

If the nature of the trend to impact is

* up
  * to disrupt it, reduce or stabilize the values of the observed, trending percept
  * to further it, increase the values of the observed, trending percept
* down
  * to disrupt it, increase or stabilize the values of the observed, trending percept
  * to further it, decrease the values of the observed, trending percept
* steady
  * to disrupt it, cause a value for the previously trending percept to change

### Indirectly impacting a percept given a causal theory

A CA can impact n percept A **indirectly** by impacting a *causally linked*, observed percept B.

* if A and B are mutually exclusive (according to the CA's causal theory) then
  * initiating B should terminate A
  * persisting B should prevent A
  * terminating B should allow for A
* if A and B must co-exist under some condition then
  * initiating B should create A
  * persisting B should persist A
  * terminating B should terminate A
* if B causes A under some condition then
  * initiating B should eventually create A
  * persisting B should persist or eventually create A
  * terminating B *might* terminate A
