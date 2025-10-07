# Research notebook

## August 20, 2025

Better framing for experiences and a rethink of the possible types of experiences. Clearer integration with wellbeing, causal theories and affordances.

## August 1, 2025

Sensor and effector CAs coded and unit tested

## June 1, 2025

Separated out Apperception Engine, Actor Model and Prolog Utils into their own repos

## May 24, 2025

Made minor edits to paper "Finding causal theories quickly enough" and published version 2 to Zenodo

## April 21, 2025

Sketched mechanisms for wellbeing osmosis and capacitance.

## April 18, 2025

Meeting with Elliott H. Discussed parametrization leading to exploit vs explore tendencies. Wellbeing diffusion across CAs and wellbeing capacitance. And the need for lower-level CAs to sometimes override the affordance dictates from on high, being closer to the ground truth though with a narrower view.

## April 17, 2025

Meeting with Avel G-C

## April 7, 2025

Cleaned up existing code to remove obsolete design elements and replace active voice (e.g. "start") with passive voice (.e.g "started")

## March 13, 2025

Work session with Elliott Hauser. Leads to a number of design changes, with removal of wellbeing and meta-cognition actors, and folding their function into the CAs themselves, for greater decentralization.

## February 18, 2025

More details on affordances, with a algorithm for their execution

## February 7, 2025

Elliott Hauser becomes project advisor

## February 4, 2025

Avel Guénin becomes project advisor

## January 2025

Progress on coding the outline of a CA's timeframe

## November 12, 2024

Coding progress: MetaCAs grow the SOM
Symposium: Presentation on "An experiment in articial agency" recorded and submitted

## October 10, 2024

Coding progress:  Improved actor model framework (added signaling and did refactoring). Meta-cognition actor is adding cognition actors

## October 02, 2024

Presented `Actors making inferences - a computatinal substrate for artificial agency` at open hour

## September 22, 2024

Commented on [A beautiful loop: An active inference theory of consciousness](https://osf.io/preprints/psyarxiv/daf5n?view_only=) and to what extent Karma fulfills the requirements for artificial consciousness.

## August 26, 2024

Completed revision of agency notes

## August 21, 2024

Presented on the project's Philosophical Stances

## August 8, 2024

Wrote about metacognition actors

## July 17, 2024

Presented an intro to the project

## July 9, 2024

Wrote about intents and action affordances.

## June 27, 2024

Clarified the nature and role of Wellbeing measures, and wrote about it.

## June 24, 2024

Formalized the nature and origins of a CA's experiences entailing the synthesis of objects, and wrote about it.

## June 23, 2024

Figured out a setup allowing for niche construction by the rover

## June 18, 2024

Wrote about the search spaces of agency

## June 16, 2024

Defined interlocking rules and constraints specifying the purpose and behavior of cognition actors

## June 9, 2024

Defined the rules by which CAs are added and culled by meta-CAs, based on competence and relevance.

## June 8, 2024

Wrote about how time manifests in a SOM.

## June 7, 2024

Deleted clock actor. Replaced by a timer thread used to delay sending messages.

## June 4, 2024

Added a clock actor that publishes tic events (WIP)

## June 3, 2024

Design: Rules and constraints for how a Meta-CA builds and adjusts the set of CAs at its level of abstraction.

## June 2, 2024

Agency start level-1 meta-cognition actor
Normalize query API of CAs
Improved payloads of prediction events and predction error messages

## June 1, 2024

### Idea for experimental setup - Dissociative learning

Two differently colored patches, only one is food. The other has no nutritional value.
Once in a while, reverse which color is food and see how the agent changes its association between color and food.

## May 23, 2024

I became Research Fellow at the Active Inference Institute thus the motivation for this notebook.

## May 27, 2024

### Agency

* Sensor CAs receive predictions, read sense value if state, send prediction errors if prediction inaccurate
* Effector CAs initialized
* Can send messages to an eccector CA to actuate
* Can tell body interface to execute pending actuations

### Body

* Added sense value tolerance (i.e. accuracy of reading)
