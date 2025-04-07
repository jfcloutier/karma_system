# The search spaces of agency

A society of mind is a collective of specialized, inter-dependent cognition actors that, together, animate an autonomous robot. A successfully evolved/evolving society of mind is one that promotes its own continuity by reliably and safely finding, via the  robot's body, sources of energy in an environment that "wants" to dissipate it.

Evolving a society of mind is a complex search problem. We can look at agency as the self-directed, concurrent exploration of multiple search spaces, internal and external to the agent. For each search space, I briefly describe what is being looked for and why.

## External search spaces

The robot searches the outside world (aka what the agent is not) for what it needs from it and for what it needs it to become.

### Resource space

* What: Searching for food while avoiding collisions
* Why: To maintain wellbeing

### Niche space

* What: Searching for how to  beneficially alter the environment
* Why: To increase predictability in exploitation and reduce risks in exploration

## Internal search spaces

The agent searches its "inner space" (aka what the agent was, is, and can become) to make sense of signals (merkwelt) and to discover affordances (wirkwelt)

### Assembly space

* What: Searching for ways cognition actors (CAs) can assemble into a working collective
  * Some background:
    * A CA deals with a subset of the agent's environment at some level of abstraction
    * A CA observes its umwelt (and nothing else) and acts on it (and nothing else)
    * A CA's umwelt is made of other CAs (subject to constraints that obligate hierarchies)
    * The most primitive CAs are sensor and effector CAs whose umwelts are the robot's sensors and motors
    * The larger the collective, the higher the energy cost to the agent
    * Conjecture: Only CAs high enough in the collective's hierarchy can detect clear wellbeing trends and discover reliably effective affordances to control these trends
* Why: To maximize control over wellbeing while minimizing energy expenditure

### Causal theory space

* What: A CA searching for causal theories it can use to successfully
  * make sense of step-wise changes in its umwelt
  * and predict future changes to it (spontaneous or from acting on it)
* Why: To maximize predictive accuracy and minimize theory complexity (Occam's Razor)

### Belief space

* What: A CA searching for regularities (or loss thereof) in its latest observations that then become its beliefs
  * For example, a CA detecting that observed distances are trending down might believe that the agent is approaching an obstacle
  * A belief is how a CAs has made sense of past observations of its umwelt
* Why: To detect signals in past observation while minimizing noise

### Affordance space

* What: A CA searching for how it can act to most effectively impact its own beliefs
  * By disrupting unpleasant (wellbeing-reducing) beliefs and promoting pleasant (wellbeing-increasing) beliefs
* Why: To increase policy effectiveness and reliability, and minimize misfires
