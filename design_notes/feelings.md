# About feelings

Remember that Cognition Actors (CAs) form a dynamic, inter-dependent and interactive collective making up the robot's mind. I am at the point in my coding where a CA associates feelings to its experiences before deciding which experience it wants most to eliminate or persist.

Feelings are essential to survival. How a CA feels directs its attention to what matters most and what needs to be acted upon in priority. Different CAs will have different feelings though feelings are contagious (more on this in a later post).

A feeling is a negative or positive scalar value. A feeling captures the values and direction of change of distinct wellbeing dimensions (fullness, integrity and engagement). A high but decreasing integrity (bad) might contribute more to the current feeling than a low but steady fullness (not good). How a CA feels might motivate it to improve its integrity at the expense of its fullness.

Feelings are computed for each timeframe of a CA's life. A timeframe is a "thick now" in which each CA executes its OODA loop. One step of the loop is to integrate into experiences the observations it made of its umwelt of CAs. The next step is to attach a feeling to each experience.

A single feeling is associated to each timeframe of a CA's lifetime. However, experiences within a timeframe can feel differently, otherwise the CA would not know which experiences need its attention the most.

An experience has, by default, the same feeling as that of the current timeframe, but an experience that has persisted across timeframes would have that default feeling modulated based on how the feelings of these timeframes have changed. An experience that persisted across timeframes with improving feelings will feel better than a new experience in the same timeframe.

Feelings are computed from wellbeing values. A CA's wellbeing values are automatically incremented or decremented during the executions of its OODA loop (getting a new causal theory costs fullness points, bumping into something costs integrity points, making successful predictions adds engagement points, consuming food adds fullness points etc.)

Feelings are computed, from current wellbeing values and how they are changing, according to these principles:

* A change in wellbeing value or its interruption is felt more strongly than its absolute value.
* A change in wellbeing value or its interruption when low is felt more strongly than a change when the value is high.
* In the absence of a change or interruption, the absolute value is felt, with low values felt more intensely than high values.

For example:

* What feels good, best first:
  * A wellbeing value trending up (from low feels better than from high)
  * A wellbeing value stabilizing from trending down (from low feels better than from high)
  * An above median wellbeing value

* What feels neutral:
  * An unchanging, median wellbeing value
* What feels bad, worst first
  * A wellbeing value trending down (from low feels worse than from high)
  * A wellbeing value stabilizing from trending up (from low feels worse than from high)
  * A wellbeing value below median

In short, the overall feeling associated to a CA timeframe (how it feels generally at the moment) integrates the contributions from each wellbeing dimension, and an experience's feeling is the feeling of the timeframe modulated by the "feeling history" of that experience.
