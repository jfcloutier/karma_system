# About time

Time manifests in interesting ways in my computational cognitive architecture.

The cognitive architecture is distributed. Nothing is centralized. There is, for starters, no central, shared time.

An agent's behavior emerges from interactions between a collective of cognition actors forming a Society of Mind (SOM). Each cognition actor tries to make sense of its own, limited umwelt so as to act on it to the agent's benefit.  The umwelt of a cognition actor is made up of other, less abstract, cognition actors, making the SOM a hierarchical structure.

Each cognition actor is a long-lived process that controls and manages its own state. A cognition actor's process interacts with other cognition actor processes strictly by asynchronously sending and receiving messages.

The SOM is an application of the Actor Model, a general model of concurrent computations, to artificial cognition.

Let's first state that a cognition actor does not know about "system time" a.k.a. the computer's clock. As far as the SOM is concerned, there is no shared time (unlike in a Newtonian universe) and, as far as a cognition actor is concerned, there is no absolute time. There's only time moving forward; there's a before and there's an after. Time moves forward for the actor whenever it receives a message that may lead it to change its process state. Cognition actors do not share a common time but they move each other forward in unmeasured time by exchanging messages.

This seems reasonable but it is not sufficient. Cognition actors need a more elaborate relationship with time; they need the notion of time frames (periodicity).

Within each time frame, a cognition actor accumulates observations (uncontested predictions plus prediction errors) and, at the end of the time frame, update its experiences (detected temporal patterns), decide whether to act, and whether to update the symbolic generative models with which it makes predictions. The more abstract a cognition actor (i.e. the further up the hierarchy), the longer its time frame will be. The state of a cognition actor with abstract experiences should change more slowly than that of bottom-level cognition actors wrapping the body's sensors. Furthermore, the time frames of cognition actors are not synchronized, that is, their boundaries do not intentionally align.

Time frames are realized by giving cognition actors the ability to send messages after set delays. For example, an actor sends itself a message to complete a time frame 2 seconds hence. Upon receiving this self-reminder, the cognition actor, updates its experiences etc. and then sends itself the same reminder, and on and on.

A cognition actor's notion of time encompasses past, present and future. The past is instantiated by the memory of prior observations, experiences and actions carried out, and by its symbolic generative model that compresses past observations into causal rules. The (extended) present exists from the beginning to the end of the current time frame during which the cognition actor interacts with others. The future is manifested by the delayed messages the cognition actor sends to its future self, and by the observations it anticipates from executing the action affordances it formulates in the present.
