# Karma is an emergent/enactive system even if it is symbolic

["Embodiment in Cognitive Systems: on the Mutual Dependence of Cognition & Robotics"](https://www.researchgate.net/publication/254400974_Embodiment_in_Cognitive_Systems_on_the_Mutual_Dependence_of_Cognition_Robotics) by David Vernon et al. compares two paradigms of empirical cognition, namely **cognitivist** systems and **emergent/enactive** systems.

*TLDR; According to this paper, I am building an embodied, emergent and enactive cognitive system. It is unusual, in part, because it is symbolic, which is widely considered a defining attribute of cognitivist systems, the other major approach.*

    The five central concepts of enactive cognitive science are embodiment, experience, emergence, autonomy and sense-making. In contradistinction to cognitivism, which involves a view of cognition that requires the representation of a given objective pre-determined world, enaction asserts that cognition is a process whereby the issues that are important for the continued existence of a cognitive entity are brought out or enacted: co-determined by the entity as it interacts with the environment in which it is embedded. The term co-determination [...] implies that the process of cognition determines what is real or meaningful for the agent.

    [...]

    Co-determination means that the agent constructs its reality (its world) as a result of its operation in that world. In this context, cognitive behaviour is inherently specific to the embodiment of the system and dependent on the system’s history of interactions, i.e., its experiences. Thus, nothing is ‘pre-given’. Instead there is an enactive interpretation: a real-time context-based choosing of relevance (i.e. sense-making). 

    [...]

    In most cognitivist approaches concerned with the building of artificial cognitive systems, the symbolic representations are initially at least the product of a human designer: the designer’s description of his view of the world. This is significant because it means that these representations can be directly accessed and interpreted by others. It has been argued that this is also the key limiting factor of cognitivist systems as these programmer-dependent representations effectively blind the system, constraining it to an idealized description that is a consequence of the cognitive requirements of human activity. This approach works well as long as the assumptions that are implicit in the designer model are valid. As soon as they are not, the system fails.  

    [...]

    Enactive systems are founded on the principle that the system discovers or constructs for itself a world model that supports its continued autonomy and makes sense of that world in the context of the system’s own morphology-dependent coupling or interaction with that world. The identification of such generative self-organizing processes is pivotal to the future progress of the field.

I have only one minor qualm with the paper: It implies that a symbolic approach is necessarily cognitivist.

    Although the use of symbols is often presented as definitive difference between the cognitivist and emergent positions, they differ more deeply and more fundamentally, well beyond a simple distinction based on symbol manipulation.

Most, if not all all, cognitivist systems rely on symbol manipulation, so I understand the belief.

However the cognitive system I am building is both emergent/enactive **and** symbolic. It is **not** cognitivist even though it is symbolic. My autonomous robot will invent symbols and assign them meaning from its experiences. As a consequence, the robot's emergent ontology will be its own. It may not even be relatable to us humans.

This still begs the question, why attempt a *symbolic* emergent/enactive cognitive system when the vast majority rely on a *connectivist* approach? Some might argue that "symbolic" and "emergent" are mutually exclusive.

An emergent/enactive cognitive system learns, on its own, a world model from interacting with its environment. Connectionist machine learning is well-understood and has had remarkable successes. A symbolic approach is typically only used to predefine world models in terms of logic rules already learned by humans. It seems it would make sense for me to rely on a connectionist approach.

That said, an enactive system capable of *inductive program synthesis* could build its own world model as logic rules. It could then use these logic rules, maybe expressed as a logic program, to make predictions and select action plans. In other words, one can envision a symbolic emergent/enactive system where histories of experiences are generalized on-the-fly, via symbolic machine learning, into predictive/generative logic programs. One advantage to this approach is the small learning set required to induce potentially competent world models (connectionist approaches require large learning sets).

My [cognitive system design](https://zenodo.org/records/17941263) relies on my [implementation of the Apperception Engine](https://zenodo.org/records/15512255) to discover/induce short logic programs on demand, programs that explain and predict the system's experiences. The search spaces of logic programs are kept manageable because the world model is distributed over a collective of cognition actors, each with a limited experiential scope.

So, it is not irrational on my part to attempt a symbolic implementation of an enactive/emergent cognitive system.

The main driver for choosing a symbolic approach is that I primarily do this work to further my own understanding of cognition. Taking a connectionist approach would lead to the creation of "black boxes" (large matrices of floating point numbers) as the system's learning artifacts. My symbolic emergent/enactive system will generate/update a distributed world model as many small logic programs, which are "white boxes". I am more likely to gain insights from studying small white boxes than large black boxes.
