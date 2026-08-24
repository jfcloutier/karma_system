# Rethinking observations from predictions

## Recap

A robot is an autonomous and mortal agent animated by an evolving collective of communicating processes called Cognition Actors (CAs). The collective captures and applies what the robot learns about how to survive. The robot learns by changing the hierarchical structure of its mind-collective and by growing the competency of the individual CAs composing it.

The collective forms an abstraction hierarchy where each CA has an umwelt composed of more "concrete" CAs that it observes, experiences, feels and acts upon. The bottom layer of CAs mediates access to the robot's sensors and motors, whereas the upper layers deal with the "big picture" of surviving.

Each CA goes through a repeated "OODA loop" cycle (once per timeframe) where it runs through a sequence of predict, observe, experience, feel, plan, act and assess steps. The more abstract the CA, the longer its timeframe. CAs run as separate, non-synchronized processes that interact with one another via queued messages.

The hope is that, from the interactions within an adaptive collective of CAs, competent agency will emerge.

## Synopsis

An autonomous agent must learn to predict what happens next in order to survive. The more informed its predictions, the more it can learn from prediction errors.

 I see five provenances for predictions, each one more informed than the other.

1. Predicting that nothing can be observed (predicting from complete absence of information)
2. Predicting that nothing last observed will change
3. Predicting that incoming observations will maintain current experiences (of counts, comparisons, unchanging and trends, as constructed from observations)
4. Predicting observations from understanding (from having a model of latent processes causing observations)
5. Predicting goal/directive activations from plans the CA built to achieve its intent and received directives

Given the provenance of a prediction, a consequent prediction error can present a learning opportunity of lesser or greater value:

1. A prediction error as completely unanticipated observation (least value because the prediction came from ignorance)
2. A prediction error as surprising observation causing a new experience (some value)
3. A prediction error as surprising observation altering or terminating an experience (more value)
4. A prediction error as surprising observation triggering the revision of a causal model (greatest value because the prediction came from understanding)
5. A prediction error as adjusted observation of a sent directive's activation status toward having been executed

When a cognition actor is created, it has everything to learn and can, at first, only predict that nothing will be observed. As it accumulates observations, then the experiencing of these observations, and the plans to impact experiences, it can make more informed predictions and thus learn more from errors. Eventually, the cognition actor will have enough of a history of observations to acquire a causal model, allowing it to make predictions from its *understanding of what causes observations*, and potentially correct this understanding from errors.

## Predictions, prediction errors and observations

In each timeframe ("thick now") of its life, a CA makes observations by emitting predictions and maybe receiving prediction errors as a consequence. One way a CA makes predictions is by developing a causal theory about the latent processes that cause what it observes, and then using this theory to predict incoming observations.

An observation is either an uncontested prediction or a prediction error consequent to a prediction.

A CA assigns a confidence (between 1% and 100%) to each prediction it sends to its umwelt CAs. It does the same with each prediction error it sends back in response to an incorrect prediction received from parent CAs.

When a CA receives a prediction that is not meaningful to it, it returns a fully confident prediction error with value `unknown`.

An uncontested prediction is one that has received no prediction error or has only received unknown-valued prediction errors from a strict subset of its umwelt (at least one umwelt CA matched the prediction with an experience).

It is possible for a prediction to not cause an observation if consequent unknown-valued prediction errors were received from all umwelt CAs; the prediction was meaningless to the entire umwelt, and thus no information about the umwelt was gained from making the prediction.

Different umwelt CAs can reply to a prediction with prediction errors that have conflicting values. Only the most confident, most informative among conflicting, value-bearing prediction errors becomes an observation. A tie is resolved by using the last prediction error received.

A prediction error that is at least as confident as the contradicted prediction overrides the prediction as observation and confers its confidence to the resulting observation.

A prediction error less confident than the prediction it corrects is dropped but it erodes the confidence in the resulting observation-from-prediction.

## Making predictions

A CA must decide which prediction(s) to make within the current timeframe.

The CA collects all the predictions it could make and drops those that fall too far below the average confidence of the lot (e.g. below half average).

The sources of predictions, in decreasing order of authority, are:

* Plans built to impact (strongly felt) experiences (**goal activation predictions**)
* Inferring from the causal theory applied to prior observations (**predicting observations from an understanding of latent processes**)
* Extrapolating from prior experiences (**predicting observations that sustain the CA's current experiences**)
* Predicting unaltered prior observations (**predicting that the umwelt did not change**)
* As a last resort, making an empty prediction (**predicting that nothing will be observed**)

When uncontested predictions conflict (different values are predicted), the one with the highest authority will be made. When conflicting predictions have equal authority, the one with highest confidence is the one that will be made.

## Predictions from plans

See [acting](../acting.md)

## Predictions from experiences

A CA synthesizes its experiences from observations it makes of its umwelt. The CA can predict a number of observations on the basis of its current experiences.

Making predictions from prior synthetic experiences (either `trend`, `count`, or `more` experiences):

* Trend: Predict an observation that continues the experienced trend by the increment/decrement recently observed
* Count: Predict the counted observations
* More: Predict the compared observations

## Empty predictions

At the start of its life, a CA has no observations, experiences, causal theory or plans. The CA can only make an empty prediction.

Each umwelt CA responds to an empty prediction with fully confident prediction errors, essentially stating each of its experiences in the form of a prediction error.

An empty prediction is always overridden by the prediction errors it causes; it never becomes an observation.

Making an empty prediction is a last resort because the consequent prediction errors provide no information to the CA about its own competency; there is no knowledge to evaluate and improve upon when a prediction is made from absence of knowledge.

## Causal theory and confidence

WWhen a CA uses its causal theory to generate a prediction from current observations, getting a prediction error as a consequence reduces the CA's confidence in the theory.

When a CA receives no prediction error from a prediction generated from its causal theory,  it gains confidence in the theory.

The confidence the CA has in its causal theory is conferred to the predictions generated using it.

## The persistence of predictions

Predictions received are temporarily "sticky". Unless overridden, an incoming prediction persists across a few lifecycles of a CA to match the longer lifecycles of its parents.

This is needed since not receiving a prediction can be just as meaningful to a CA as receiving one.
For example, not receiving predictions about the activation of a directive indicates that parent CAs are no longer interested in pursuing it.

A persisted prediction is as active as a just-received one.
It is possible for a prediction received by a CA in its lifecycle T to cause it to send a prediction error but only in lifecycle T+1, because of a change in the CA's experiences from T to T1.
