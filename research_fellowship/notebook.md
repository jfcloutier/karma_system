# Research notebook

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
