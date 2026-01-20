# Synthesizing experiences from observations

Integrate current and past observations into experiences by:

* synthesizing as many `count`, `more` and `trend` experiences as time allows
* then elevating all unused observations as experiences

## Value domains

* count: 1, 2, 3, `many`
* more: another synthetic object
* trend: `up`, `down`, `ended`

## Synthesizing experiences

* Before work, update prior experiences and assign their confidences
  * A prior experience may no longer exist,
  * or a trend may take value `ended`
  * or a count may take value 1
* In each unit of work, find a novel experience and assign a confidence

## Finding a novel experience

* Choose in order a kind from [count, more, trend]
* Find a non-empty, maximal set of observations to which the kind applies
* The maximal set of observations defines a synthetic object as the origin of the property/relation
  * count: 2 or more countables:
    * Identical properties (same origin, kind and value)
    * Properties with same kind and value
    * Relations with same kind and value object
    * Relations with same kind and origin
  * more: 2 non-equal comparables (each a different maximal set of observations)
    * Properties with same kind and value X 2 (more * --P-> value A than * --Q-> value B)
    * Relations with same kind and value object X 2 (more * --X-> object A than * --Y-> object B - there are more objects with relations X to object A than there are objects with relation Y to object B)
    * Relations with same kind and origin X 2 (more object A --X-> * than object B --Y-> * - object A has more relations X than object B has relations Y)
  * trend: 2 or more trendables over the last N > 1 time frames
    * Properties with the same origin and kind
      * If values are numerical, the values can be `up`, `down`
      * Otherwise, if a trend stopped, its value is `ended`

## Assigning a confidence to an experience

* Take the minimum confidence in the observed set(s) composing the synthetic object(s) of the experience (don't multiply)
* if a trend, decrease the minimum confidence C by C/N where N is the number of trending observations

## Elevating unused observations

* Select all observations not composing objects of current experiences
* Add them as experiences with unchanged confidence
