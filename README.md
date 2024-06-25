# karma_system

This repository is an umbrella for the `sym-cog-robotics` research project of the Active Inference Institute that I am conducting as a Research Fellow.

The name of the software system under development is Karma. [Why the name](https://en.wikipedia.org/wiki/Karma)

> Karma [...] is a concept of action, work, or deed, and its effect or consequences> In Indian religions, the term more specifically refers to a principle of cause an> effect, often descriptively called the principle of karma, wherein individual> intent and actions (cause) influence their future [...]

Here are key concepts and opinions shaping this effort:

* **Active Inference** - an agent must behave *as if* it actively minimizes surprise to preserve its identity
* **Enactivism** - cognition arises through a dynamic interaction between an agent and its environment, and an agent's perceptions and actions are constructively co-dependent
* **Apperception** - predictive sense-making is realized by the discovery of unified causal theories
* **Mortal Computing** - meaning is grounded in the agent's drive to survive
* **Society of Mind** - agency is realized by a collective of cognition actors interacting with each other and the agent's environment
* **Kantian Whole** - the parts (cognition actors) exist for and by means of the whole (the society of mind)
* **Constraint Closure** - a cognition actor constrains how the society of mind can change, and vice-versa
* **Autopoeisis** - an agent's society of mind is a continuous process of self-production and self-maintenance

The code of the Karma project is distributed over these repositories

* [Karma Agency](https://github.com/jfcloutier/karma_agency) - Prolog code implementing agency
* [Karma Body](https://github.com/jfcloutier/karma_body) - Elixir code giving access to the robot's sensors and motors, embodied or simulated
* [Karma World](https://github.com/jfcloutier/karma_world) - Elixir code implementing a virtual, simulation environment - to accelerate the development of Agency
* Karma Observer - TBD - Code providing an outsider's view on the robot's cognition
* Karma Analyst - TBD - Code facilitating analysis of data gathered from running the robot

The objective of this project is to explore *one* way to implemnt artificial basal cognition.

If successful, the software will animate an autonomous rover that can learn, on its own and starting with minimal a priori knowledge, how to survivably engage its environment by progressively making sense of it and discovering its affordances.

Though it implements a computational model of embodied cognition -software running on mobile hardware-, this effort must not be construed as supporting the view that cognition in *living* beings is computational. I don't believe it is.
