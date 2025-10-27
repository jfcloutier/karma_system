# Active Inference Institute Research Fellows Application

## Cover letter

Active Inference Institute
Research Fellows Program

May 3, 2024

Greetings,

I am applying for a Research Fellowship at the Active Inference Institute. As a Research Fellow, I would carry out research in Symbolic Cognitive Robotics.

I am a member of the AII since 2022. I lead the AII's Symbolic Cognitive Robotics research project. I was a speaker at the Second and Third Annual Active Inference Symposium.

My research would be the continuation of a project of many years in which I program simple autonomous robots to develop and ground my understanding of concepts in Cognitive Science.

I am constantly surprised by the questions this exploratory work has raised and keeps raising. Looking for answers has already taken me on an unanticipated journey, both within and beyond Active Inference. I have been drawn into Active Inference of course but also Kantian epistemology, the issue of map vs territory, biosemiotics, mortal computing, collective intelligence, autopoesis and constraint closure.

Always at the forefront is how these alternative perspectives/theories/frameworks intersect and contrast with Active Inference. I would add that these epistemological excursions are always in the service of, and thus are contained by, the telos of writing software that works.

I am grateful for all the support I have already received from the AII. I am applying because I trust my research would greatly benefit from the additional mentoring and structured engagement that comes from being a Research Fellow.

I intend to continue as principal investigator of the Symbolic Cognitive Robotics project, and I remain eager to share my thoughts and findings with other members of the AII via Coda and Discord, and more widely, via live presentations and self-published papers, or in other ways the AII deems beneficial

Best regards,

Jean-François Cloutier

jean.f.cloutier@gmail.com

<div style="page-break-after: always;"></div>

## Application

### Title

Symbolic cognitive robotics

### Abstract

The project asks What does it take, at a minimum, for a robot to learn, on its own, how to survive in a world it knows initially almost nothing about?

It is an exploration of artificial basal cognition, with an emphasis on autonomous, *symbolic* learning. The exploration is anchored in the programming of simple robots. The intent is to shed light on the computational processes needed to instantiate agency and make possible sense making via active and embodied engagement.

Active Inference is here considered an *as-if* framework, one in which a self-maintaining agent must, to an external observer, *appear* to behave as if it minimizes current and future surprisal. Other perspectives are brought in to inform the *implementation* of an artificial agent, namely logic, functional and actor computing, biosemiotics [1], collective intelligence [2] [3], constraint closure [4] [5], and applied Kantian epistemology [6] [7].

The deliverables of the project are an open-source software implementation, an Active Inference analysis of observations collected from running the robot, findings about the dynamic properties and capabilities of the implementation, and a discussion on the value of taking a multi-paradigmatic approach to cognition.

### History

This project is a multiyear personal endeavor, started in 2016, to explore concepts of cognition through the programming of simple Lego EV3 robots.

In 2022, my work found a home at the Active Infererence Institute as the the Robotics and Embodied research project. Its prior history was presented in 2022 at the Second Annual Active Inference Symposium [8].

In 2023, an update on the latest iteration of the project was presented and the Third Annual Active Inference Symposium [9].

In 2024, the project's name was changed to Symbolic Cognitive Robotics. It is currently active and I am, for the moment, the sole investigator.

### Assumptions

This research project makes a number of key assumptions:

* Active Inference is an as-if framework[10]; it *prescribes that* an autonomous, self-maintaining agent must minimize surprisal through behavior and experience updating. However it does not *prescribe how* such agency is implemented.

* All intelligence is collective intelligence [2]; it is from the interplay of cognitive parts that emerges an agent's purposeful and intelligent behavior.

* Intrinsic sense-making [11] (residing in the agent and not its programmers or observers) is grounded in the survival imperative [12].

* Sense-making can be realized by the discovery of causal theories induced from limited observations (via a type of symbolic of machine learning that can be done quickly and with very little data).

* Symbolic reasoning, as opposed to artificial neural networks and other purely probabilistic approaches, is sufficient to implement intrinsic sense-making and agency.

### Questions

I realize that each of the (interlocking) questions below could be the basis of a long-term research program. My intent is nonetheless not entirely immodest. I only seek to scratch many surfaces at once by attempting to program an autonomous robot that exhibits basal cognitive abilities, and, in the process, hopefully shed some light.

* Can  a simple robot (a Lego rover robot) be programmed such that it demonstrates *intrinsic* sense making via autonomous engagement with its "umwelt"?

* What is the umwelt of a rover robot as it appears to the robot?

* Can agency be *programmed*, or is this a contradiction in terms?

* Can Kantian apperception be the basis for the predictive processing capabilities of an autonomous robot?

* Can "artificial apperception" operate in "useful time", that is, while the robot is engaging its world?

* How does the predictive accuracy of causal theories -obtained from apperception- relate to perceptual precision?

* How are symbolically-expressed experiences formed from remembered perceptions, and how does the precision of perceptions transfer to experience certainty?

* Can an external observer make sense of the intrinsic experiences of an agent?

* How is normativity determined so that a robot can distinguish between desirable and undesirable experiences?

* What mechanisms relate normativity and experience certainty to attention?

* How does attention constrain apperception?

* What role do feelings, as homeostatic signals, play in assigning normativity to experiences?

* How are feelings generated and communicated internally?

* How and when are action plans synthesized from simpler actions?

* How are actions evaluated for their effectiveness at acquiring new experiences, invalidating undesirable experiences and challenging desirable experiences?

* Can cognition be realized as a collective of simple parts -cognition actors-, each with its own limited "umwelt" and action repertoire?

* How are experiences abstracted within the collective, namely how do the *experiences* of a cognition actor become the *perceptions* of another, more abstract, cognition actor?

* How is consensus realized within a collective of cognition actors as to what actions the robot should take next?

* How does each cognition actor learn individually, and how does the collective evolve structurally from processing the robot's dynamic experiences?

* What constraints are needed to reduce the number of possible trajectories a collective of cognition actors could take in its evolution?

* If sense-making is grounded in the survival imperative, how can experiments be designed such that a robot somehow faces its own demise unless it learns to achieve self-maintenance?

* Can Active Inference analysis be done on experimental data to validate whether or not the robot is indeed minimizing surprisal?

* What data must be collected to enable such analysis? How is the analysis conducted?

* What constitutes evidence of surprisal minimization by the robot, in the short term and in the long term?

### Objectives and method

The overall objective of this research is to gain a better understanding of (models of) cognition by grounding this understanding in computer programs that animate physical robots. Programs have the advantageous property of being fully-described and unambiguous, else they don't compile!

I intend to shed some light on the questions listed above by building and embedding software on an autonomous robot, a rover, in order to impart it with basal cognitive capabilities, with a focus on unsupervised learning.

The computational properties of the software and the behavior of the rover will be observed and analysed. Of interest will be whether, why and how the evolution of cognition actors -and of the collective they form- converges toward greater competency as the robot attempts to survive via active engagement.

Of equal interest will be whether collected experimental data can be subjected to analysis under the Active Inference framework to determine the extent to which a robot demonstrates a clear tendency to minimize surprisal.

To be successful, the software must implement a number of capabilities. Depending on the nature of these capabilities, logic programming (in Prolog) or functional programming (in Elixir) is being used. Furthermore, the implementation is distributed across more than one computer. The embodiment-related functions, written in Elixir, reside on the robot's computer, a Raspberry Pi3. The more computationally intensive code that implements agency is written in Prolog. It resides on a much more powerful computer, not on the robot. The separately-hosted software components are networked to enable them to communicate with each other and, together, realize an embodied agent.

To accelerate the development and testing of agency functions, a simulated embodiment (virtual sensors and effectors) and a simple virtual world are implemented in Elixir and run on a computer also not on the robot.

### Significance and impact of the proposed research

The proposed research aligns with the mission of the Active Inference Institute as an "open-science institute dedicated to improving the accessibility, rigor, and applicability of the Active Inference framework."

The research tests an alternative approach to implementing Active Inference agents, one that uses symbolic machine learning (founded on Kantian apperception) instead of the probabilistic modeling formulated by the free-energy principle.

It uses the construction of robotic software as an integrative means to explore concepts of embodied agency, sense making, active engagement, all contributing to and predicated upon self-directed learning.

The open-sourced software built in this project will be instrumented to produce experimental data that will be subjected to analysis under the Active Inference framework. If successful, this will provide an additional instance [13] of an empirical application of the free-energy principle.

### Timeline and milestones

The project is divided in three phases:

1. Software development and robot design (1 year elapsed)
2. Collection of experimental data and revisions to software/robot (6 months elapsed)
3. Instrumentation and Active Inference analysis of collected data (6 months elapsed)

#### Software development and robot design

##### Already completed

* Access to the sensors and effectors of an EV3 Lego robot (Elixir)

* Implementation of virtual sensors and effectors

* Implementation of a simple virtual world

* Network integration

* Predictive processing via a high-performance apperception engine to discover causal theories from past perceptions [7]

* An actor model framework with which to implement a dynamic collective of cognition actors

##### In progress

* A mechanism for initializing the collective of cognition actors from knowledge of sensors and effectors embedded on the robot

* Feelings computation, updating and signaling

* Cognition actor logic (prediction, perception, experience updating, action synthesis)

* Metacognition logic (cognition actor creation, competency evaluation, destruction)

* Lego EV3 rover robot design

#### Collection of experimental data

* Experimental design

* Data collection and monitoring capabilities added to the software

* Experimental runs and data collection

#### Active Inference analysis of the experimental data

* Analysis process design

* Analysis of the data to determine compliance with the free-energy principle

* Visualization and discussion of findings

### People and institutions involved

I am currently the sole investigator. Participation is welcome. No institution other than the AII is involved.

### Dependencies and contingencies

The needed robotic and computing equipment is already acquired. All software used in this project is open-sourced and freely available.

The work will be carried out on a part time basis, with on average 1.5 days a week dedicated to it.

<div style="page-break-after: always;"></div>

## Resume

Jean-François Cloutier, MSc

jean.f.cloutier@gmail.com

### Status

Resident of Portland, ME, USA

Canadian citizen

USA Permanent Resident

### Affiliations

Member of the Active Inference Institute

Aikido of Maine - 2nd degree black belt

### Employment

2018-present Smartrent (USA) - Senior Embedded Software Engineer

2016-2018 Starlit Software (USA) - Senior Software Architect

2005-2014  Mind-Alliance Systems (USA) - Chief Technologist

1993–2003 Noonetics/Home Information Services (USA, Canada, Belgium) - Technology manager and principal consultant

1990–1993 Transaction Technology, Inc. (USA) - Principal Member of Technical Staff

1989–1990 Zuniq Corp. (Canada) - Coordinator, R&D

1988–1989 Systems Designers Intl. (UK and USA) - Artificial Intelligence Products Engineer

1982–1988 Quebec Ministry of Education (Canada) - Consultant, researcher, course developer, teacher

### Recent presentations

Active Inference Symposium, 2023 - Growing a collective of theorizers, first steps [9]

Active Inference Symposium, 2022 - Toward a symbolic implementation of Active Inference for Lego robots [8]

Greater Than Code podcast, 2019, episode 114

ExploreDDD 2019 – Robots Modeling the Minds of Robots

ExploreDDD 2018 – Rethinking How my Robots Think

ElixirDaze 2017- Building Communities of Smart Things Takes Nerves

ExploreDDD 2017 – Modeling the Mind of an Autonomous Robot

Elixir Fountain podcast, 2016–04–11

ElixirDaze 2016 – Adventures in Robotics with Elixir

### Education

#### 1978–1988 McGill University

**B.Sc. Physiology**, McConnell Entrance Prize, twice University Scholar, once Faculty Scholar

**M.Sc. Computer Science**, full NSERC scholarship, thesis “Object-Oriented Prolog, design and implementation issues” - Graduated with Great Distinction

#### 1976–1978 Upper Canada College

High School Diploma with Governor General’s Silver Medal (Academic Head Boy)

McLaughlin Scholarship (renamed Quebec Scholarship)

Member of the school’s debating team (1978 Ontario champions)

<div style="page-break-after: always;"></div>

## Cited references

[1] Deely, John. (2019). INNENWELT AND UMWELT. Visnyk of the Lviv University Series Philosophical Sciences. 3-16. 10.30970/vps.21.2019.1. [link](https://www.academia.edu/47728077/_Innenwelt_and_Umwelt_by_John_Deely)

[2] J. Benjamin, Falandays ; Kaaronen, Roope Oskari ; Moser, Cody et al. All Intelligence is Collective Intelligence. In: Journal of Multiscale Neuroscience. 2023 ; Vol. 2, No. 1. pp. 169-191. [link](https://researchportal.helsinki.fi/en/publications/all-intelligence-is-collective-intelligence)

[3] J.-F. Cloutier, “Presentation - All Intelligence is Collective Intelligence”, May 27, 2023. [link](https://zenodo.org/records/7976317).

[4] Montévil M, Mossio M. Biological organisation as closure of constraints. J Theor Biol. 2015 May 7;372:179-91. [link](https://pubmed.ncbi.nlm.nih.gov/25752259/)

[5] Nave, Kathryn. A Drive to Survive : The Free Energy Principle and the Meaning of Life. MIT Press. (2024) [link](https://osf.io/preprints/psyarxiv/ds9mn)

[6] Richard Evans, Jose Hernandez-Orallo, Johannes Welbl, Pushmeet Kohli, Marek Sergot. Making sense of sensory input (2020) [link](https://arxiv.org/abs/1910.02227)

[7] Evans, Richard. The Apperception Engine. In Hyeongjoo Kim & Dieter Schönecker (eds.), Kant and Artificial Intelligence. De Gruyter. pp. 39-104 (2022). [link](https://philarchive.org/rec/EVATA)

[8] J.-F. Cloutier, “Toward a symbolic implementation of Active Inference for Lego robots”. Zenodo, Jul. 19, 2022. [link](https://zenodo.org/records/6862636)

[9] J.-F. Cloutier, “Finding causal theories quickly enough - building a responsive Apperception Engine”, Zenodo, Dec. 2023. [link](https://zenodo.org/records/10325868)

[10] Andrews, Mel.  The Math is not the Territory: Navigating the Free Energy Principle. (2021)  [link](https://philsci-archive.pitt.edu/id/eprint/18974)

[11] Froese, Tom & Taguchi, Shigeru (2019). The Problem of Meaning in AI and Robotics: Still with Us after All These Years. Philosophies 4 (2):14. [link](https://philpapers.org/rec/FROTPO-14)

[12] Alexander Ororbia, Karl Friston. Mortal Computation: A Foundation for Biomimetic Intelligence
 arXiv:2311.09589 (2023) [link](https://arxiv.org/abs/2311.09589)

[13] Isomura, T., Kotani, K., Jimbo, Y. et al. Experimental validation of the free-energy principle with in vitro neural networks. Nat Commun 14, 4547 (2023). [link](https://doi.org/10.1038/s41467-023-40141-z)
