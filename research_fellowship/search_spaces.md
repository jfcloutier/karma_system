# The search spaces of agency

A society of mind is a collective of specialized, inter-dependent cognition actors that, together, animate an autonomous robot. A successfully evolved/evolving society of mind is one that promotes its own continuity by reliably and safely finding, via the  robot's body, sources of energy in an environment that "wants" to dissipate it.

I will report on the rules and constraints later. For now, I'd like to share some thoughts about how evolving a society of mind is in fact a complex search problem.

We can look at agency as the self-directed, concurrent exploration of multiple search spaces, internal and external to the searching agent. For each search space, I briefly describe what is being looked for and why.

## External search spaces

The robot searches the outside world (aka what it is not) for what it needs from it and for what it needs it to become.

### Resource space

* What: Looking for food while avoiding collisions
* Why: To maintain fitness

### Niche space

* What: Looking for how to  beneficially alter the environment
* Why: To increase predictability in exploitation and reduce risks in exploration

## Internal search spaces

The agent searches its "inner space" (aka what it was, is, and can become) to make sense of signals (merkwelt) and to discover affordances (wirkwelt)

### Assembly space

* What: Looking for ways cognition actors (CAs) can assemble into a working collective
  * Some background:
    * A CA deals with a subset of the agent's environment at some level of abstraction
    * A CA observes its umwelt (and nothing else) and acts on it (and nothing else)
    * A CA's umwelt is made of other CAs (subject to constraints that obligate hierarchies)
    * The most primitive CAs are sensor and effector CAs whose umwelts are the robot's sensors and motors
    * The larger the collective, the higher the energy cost to the agent
    * Conjecture: Only CAs high enough in the collective's hierarchy can detect clear fitness trends and discover reliably effective affordances to control these trends
* Why: To maximize control over fitness while minimizing energy expenditure

### Affordance space

* What: Looking for how a CA can most effectively impact its own beliefs
  * By disrupting unpleasant (fitness-reducing) beliefs and promoting pleasant (fitness-increasing) beliefs
    * A belief is how a CAs has made sense of observations on its umwelt
* Why: To increase policy effectiveness and reliability, and minimize misfires

### Causal theory space

* What: Looking for causal theories a CA can use to successfully
  * make sense of past changes in its umwelt
  * and predict future changes to it (spontaneous or from acting on it)
* Why: To maximize predictive accuracy and minimize theory complexity (Occam's Razor)
