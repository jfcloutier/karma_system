# Building plans

A Cognition Actor (CA) seeks, through the execution of plans, to persist pleasant experiences it has and to terminate its unpleasant experiences.

## The logic of plans

A CA builds a plan when it has identified an experience it holds that need impacting (an intended goal), or when it receives a higher priority plan (as a set of directives) from a parent CA. When receiving directives "from above", it determines which goals are relevant to it; the others are likely relevant to sibling CAs participating in the same umwelt.

Goals name umwelt experiences and the desired impacts (initiate, persist or terminate). It is *entirely* up to the goal-receiving umwelt CA to construct a plan for the experiences it wants to or has been requested to impact.

Once a CA has identified (or been told by a parent CA of) an experience to initiate, persist or terminate, the CA must determine its own plan to achieve this goal. The composition of the plan depends on the type of experience and on the desired impact (initiate/persist/terminate). The plan's priority depends on the CA's wellbeing (value and gradient) if originating with the CA, or on the priority of the received directive.

How to impact an experience depends on how it was arrived at. A constructed (aka synthetic) experience is composed of observations (its base of support) which are themselves umwelt experiences the CA observed. To impact an experience a CA holds, the CA needs to impact experiences held in its umwelt.

A CA may have a causal theory. At first, it has none. At some point, the CA ask sthe Apperception Engine for a causal theory informed by its history of observations of its umwelt.

The CA can use its causal theory to predict changes to the experiences of its umwelt (i.e. incoming observations) as a result of realizing directives. This can be put to use when constructing a plan.

A causal theory has three kinds of rules

* Constraints: What is expected *never* to be observed simultaneously - e.g. not (A and B) now
* Static rules: What is expected to *always* be observed simultaneoulsy - e.g. if A and B and then also C now
* Causal rules: What is expected to be observed *next* given what was observed previously - e.g. A and B then C next

An additional but implied rule is that a previous observation survives as a current observation if it does not contradict any constraint or static rule.

A CA's abstract experience integrates multiple observations (predicted experiences in the CA's umwelt), either within the bounds of the current timeframe (`count`, and `more` experiences)
or of past *and* current timeframes (`trend` experiences).

The observed umwelt experiences involved in the composition of an abstract experience constitute the base of support of that experience. To impact an abstract experience it holds, a CA directs its umwelt to impact experiences from which the held experience is derived and perhaps also to initiate new experiences.

Since observations by the CA are experiences held in the umwelt of the CA, one can see how acting becomes a recursive operation that will unfold across multiple layers of CAs and over multiple CA timeframes, until effector CAs (on the lowest level of the hierarchy of CAs) become involved and the agent's relationship with its environment is modified by running motors etc.

The task of constructing a plan -in order to impact an experience held by the CA- consists in deciding which observed umwelt experiences to impact and how.

There will likely be different combinations of umwelt experiences that could be impacted and thus there could be many alternate plans to choose from.

The causal theory, a model of the generative processes causing these observations, if present, informs the CA in the construction of hopefully effective plans by anticipating their consequences.

To recap, the CA can seek to impact an experience it holds by impacting causative experiences held in its umwelt.
This is achieved indirectly by the CA directing its umwelt to find a way to impact these experiences in prescribed ways (initiate vs persist vs terminate).

The only types of experiences that can be impacted are `count`, `more` and `trend` experiences;
sensor CAs can not be asked to change what they perceive, activation experiences are records of actions takens, and a causal theory can not be told to imagine something else.

A sensing experience (e.g. distance(ir_sensor_1, 10)) is a record of a sensor reading already taken. There is no point denying it. The same applies to action experiences (e.g. spin(motor_1, true)). There is also no point in denying it happened. An imagined experience is one abduced by the Apperception Engine to unify a causal theory. It must be accepted for as long as the causal theory is being used.

A CA seeking to impact an umwelt experience causing an experience it holds can do so *directly* or *indirectly*.
Since synthetic experiences are composed of experiences observed in the umwelt which can themselves be synthetic experiences, a plan might be realized by more (lower-level) plans and so on until we reach only goals that can be directly impacted by activating effectors.

### Building a plan to impact an experience

How a CA might **directly** impact a held experience is modulated by the kind of experience it is.

#### Impacting a `count` experience

A `count` experience encapsulates how many of a given kind of experiences observed in its umwelt there are (for e.g., this motor was spun once).

To persist a count experience, a CA's plan would direct its umwelt CAs to persist *all of* the counted (observed) experiences.

To initiate or terminate a count experience, a CA's plan would direct its umwelt CAs to to add a counted experience or terminate *any of* the counted experiences.

#### Impacting a more experience

A `more` experience expresses that there is more of than another in its umwelt.

To initiate or teminate a more experience, a CA's plan would direct its umwelt to initiate or to terminate a compared, count experience.

To persist a more experience, a CA's plan would direct its umwelt CAs to persist both compared counts.

#### Impacting a trend experience

A `trend` experience captures how a given kind of observed experience is changing across the latest timeframes of the CA, for example, "distance keeps diminishing" is a "down" trend.

To initiate a trend experience, a CA's plan could change the ordinal value of the trending umwelt experience.
To persist a trend experience, a CA's plan would direct its umwelt to **further** the trend.
To terminate a trend experience, a CA's plan would direct its umwelt to **disrupt** the trend.

How a trend experience is impacted depends on the assigned value of the trend (up, down, same or ended).

An `up` trend captures an upwardly changing ordinal value for a given property of a given object.
A `down` trend captures a downwardly changing ordinal value for a given property of a given object.
An `ended` trend captures an unknown ordinal value for a given property of a given object after it trending.

If the nature of the trend to impact is

* up
  * to disrupt it, reduce or stabilize the values of the observed, trending experience
  * to further it, increase the values of the observed, trending experience
* down
  * to disrupt it, increase or stabilize the values of the observed, trending experience
  * to further it, decrease the values of the observed, trending experience
* ended
  * to disrupt it, cause a value for the previously observed, trending experience to stay the same or become unknown

### Indirectly impacting an experience given a causal theory

A CA can impact an experience A **indirectly** by impacting a *causally linked*, observed experience B.

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
