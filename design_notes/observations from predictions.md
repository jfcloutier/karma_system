# Rethinking observations from predictions

## Recap

A robot is an autonomous and mortal agent animated by an evolving collective of communicating processes called Cognition Actors (CAs). The collective captures and applies what the robot learns about how to survive. The robot learns by changing the hierarchical structure of its mind-collective and by growing the competency of the individual CAs composing it.

The collective forms an abstraction hierarchy where each CA has an umwelt composed of more "concrete" CAs that it observes, experiences, feels and acts upon. The bottom layer of CAs mediates access to the robot's sensors and motors, whereas the upper layers deal with the "big picture" of surviving.

Each CA goes through a repeated "OODA loop" cycle (once per timeframe) where it runs through a sequence of predict, observe, experience, feel, plan, act and assess steps. The more abstract the CA, the longer its timeframe. CAs run as separate, non-synchronized processes that interact with one another via queued messages.

The hope is that, from the interactions within an adaptive collective of CAs, competent agency will emerge.

## Synopsis

An autonomous agent must learn to predict what happens next in order to survive. The more informed its predictions, the more it can learn from prediction errors.

 I now see four provenances for predictions, each one more informed than the other.

1. Predicting that nothing can be observed (predicting from complete absence of information)
2. Predicting that nothing last observed will change
3. Predicting that observations will maintain current experiences (of counts, comparisons or trends, synthesized from observations)
4. Predicting observations from understanding (from having a causal model)

Depending on the provenance of a prediction, a consequent prediction error will be more or less informative and thus provide a greater or lesser learning opportunity to the cognition actor.

1. A prediction error provides a completely unanticipated observation
2. A prediction error can provide an observation creating a new experience
3. A prediction error can alter or terminate an experience
4. A prediction error can trigger the revision of a causal model

When a cognition actor is created, it has everything to learn and can only predict that nothing will be observed. As it accumulates observations and then the experiencing of these observations, it can make more informed predictions. Eventually, the cognition actor will have enough of a history of observations to acquire a causal model, allowing it to also make highly informed predictions from understanding.

## Predictions, prediction errors and observations

In each timeframe ("thick now") of its life, a CA makes observations by emitting predictions and maybe receiving prediction errors as a consequence. One way a CA makes predictions is by developing a causal theory about the latent processes that cause what it observes, and then using this theory to predict incoming observations.

An observation is either an uncontested prediction or a prediction error consequent to a prediction.

A CA assigns a confidence (between 1% and 100%) to each prediction it sends to its umwelt CAs. It does the same with each prediction error it sends back in response to an incorrect prediction received from parent CAs.

When a CA receives a prediction that is not meaningful to it, it returns a fully confident prediction error with value `unknown`.

An uncontested prediction is one that has received no prediction error or has only received unknown-valued prediction errors from a strict subset of its umwelt (at least one umwelt CA matched the prediction with an experience).

It is possible for a prediction to not cause an observation if consequent unknown-valued prediction errors were received from all umwelt CAs; the prediction was meaningless to the entire umwelt, and thus no information about the umwelt was gained from making the prediction.

Different umwelt CAs can reply to a prediction with prediction errors that have conflicting values. Only the most confident among conflicting, value-bearing prediction errors becomes an observation. A tie is resolved by using the last prediction error received.

A prediction error that is at least as confident as the contradicted prediction overrides the prediction as observation and confers its confidence to the resulting observation.

A prediction error less confident than the prediction it corrects is dropped but it erodes the confidence in the resulting observation-from-prediction.

## Making predictions

A CA must decide which prediction(s) to make within the current timeframe.

The CA collects all the predictions it could make and drops those that fall too far below the average confidence of the lot (e.g. below half average).

The sources of predictions, in decreasing order of authority, are:

* Inferring predictions by applying the causal theory to prior observations (**predicting observations from an understanding of latent processes**)
* Extrapolating from prior experiences (**predicting observations that sustain the CA's current experiences**)
* Predicting unchanged prior observations (**predicting that the umwelt did not change**)
* As a last resort, making an empty prediction (**predicting that nothing will be observed**)

When uncontested predictions conflict (different values are predicted), the one with the highest authority will be made. When conflicting predictions have equal authority, the one with highest confidence is the one that will be made.

## Predictions from experiences

A CA synthesizes its experiences from observations it makes of its umwelt. The CA can predict a number of observations on the basis of its current experiences.

Making predictions from prior synthetic experiences (either `trend`, `count` or `more` experiences):

* Trend: Predict an observation that continues the experienced trend by the increment recently observed
* Count: Predict the counted observations
* More: Predict the compared observations

## Empty predictions

At the start of its life, a CA has no observations, experiences or causal theory. The CA can only make an empty prediction.

Each umwelt CA responds to an empty prediction with fully confident prediction errors, essentially stating each of its experiences in the form of a prediction error.

An empty prediction is always overridden by the prediction errors it causes; it never becomes an observation.

Making an empty prediction is a last resort because the consequent prediction errors provide no information to the CA about its own competency; there is no knowledge to evaluate and improve upon when a prediction is made from absence of knowledge.

## Causal theory and confidence

WWhen a CA uses its causal theory to generate a prediction from current observations, getting a prediction error as a consequence reduces the CA's confidence in the theory. 

When a CA receives no prediction error from a prediction generated from its causal theory,  it gains confidence in the theory.

The confidence the CA has in its causal theory is conferred to the predictions generated using it.
