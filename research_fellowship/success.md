# Project success matrix

## System

| What  | Rationale | Status  | Success criteria | Risks and unknowns |
|-------|-----------|:------:|------------------|--------------------|
| **System design** | Archiecture | Initial | Identifies sub-systems, responsibilities and APIs | Boundaries misplaced, missing pieces |
| **World sub-system** | Simulated and real environment dynamics | Minimal simulation functional | * Robots can learn in a simulated world<br/> * Can animate a RL environment | Construction of a dynamic RL environment requires programmable illuminated tiles |
| **Body sub-system**| Provides an API to access physical (Lego EV3) and virtual sensors and effectors | Completed | All needed sensor and effector types covered | |
| **Agency sub-system** | Implements agency for a Lego EV3 rover | In progress | * The rover autonomously engages its environment<br/> * A mortal collective of sense-making/active cognition actors (CA) evolves <br/> * A survivable configuration of CAs is eventually found | Insufficient design, infeasibility, computationally intractable |
| **Observer sub-system** | Tooling and UI allowing a human observer to track and make some sense of the agent's autonomous behavior and learning | TBD | * Agency's behaviors and state changes are understandable<br/>* Meaningful patterns are made visible | Can the internals of agency be made comprehensible? |

## Agency

| What  | Rationale | Status  | Success criteria | Risks and unknowns |
|-------|-----------|:-------:|------------------|--------------------|
| Apperception engine in SWI-Prolog + CHR | Making sense of a dynamic environment by an engaged agent | Works | * Derives simple causal models from observations<br/> * On-the-fly traning<br/> * Operates in useful time <br/> * Not problem-specific | Will it make sense of the observations/actions of a CA? |
| Actor model framework | Adds actor model semantics to SWI-Prolog to implement CAs as actors (independent, message-exchanging processes) | Works | * Expressive<br/> * Performant<br/> * Robust | Is SWI-Prolog's implementation of threads (on which the framework depends) itself performant and robust? |
| Conceptual design | Defining the key concepts of agency (observing, sense-making, believing, evaluating, acting, and learning) | Coverage | Informs and constrains implementation | Complete, sufficient, consistent, can be operationalized? |
| Implementation | Make it work | Early progress | The agent learns to engage its environment survivably | Intractable complexity, bugs, lacking performance etc. |
