# Synthesizing experiences from observations

A dynamic CA integrates current and past observations into experiences by:

* updating, and possibly dropping, synthetic experiences from the previous timeframe
* synthesizing as many new `count`, `more` and `trend` experiences as time allows (the experiencing phase of a CA lifecycle is timeboxed)

## Value domains

* count: 1, 2, 3, `many`
* more: another synthetic object
* trend: `up`, `down`, `steady`

## Synthesizing experiences

* Before work, update prior experiences and assign their confidences
  * A prior experience may no longer exist,
  * or a count may take value 1 (counts are initially detected with values > 1)
* In each unit of work, find a novel experience and assign a confidence

## Finding a novel experience

* Choose in order a kind from [count, more, trend]
* Find a non-empty, maximal set of observations to which the kind applies
* The maximal set of observations defines a synthetic object as the origin of the property/relation
  * count: 2 or more countable observations with
    * identical properties (same origin, kind and value)
    * or properties with same kind and value
    * or relations with same kind and value object
    * or relations with same kind and origin
  * more: any 2 non-empty sets of countables, of different sizes (one set can have a count of 1)
  * trend: from 2 or more observations over the last N > 1 time frames such that
    * they have properties of the same kind, have compatible origins, and have ordinal values
      * origins are compatible if their evidence, the sets of observations synthesized, are equal or one is a strict subset of the other
    * The values can be seen to go `up`, `down` or stay `steady`

## Assigning a confidence to an experience

* Take the minimum confidence in the observed set(s) composing the synthetic object(s) of the experience (don't multiply).
* If a `trend`, boost the minimum confidence with the number of continuous trending observations.
