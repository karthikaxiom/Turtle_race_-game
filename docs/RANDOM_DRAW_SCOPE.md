# Random Draw Scope

A movement distance is sampled separately for each turtle when that turtle reaches its `forward()` call.

The random draw is therefore inside the participant loop rather than once per outer race iteration. A single pass can consequently give different turtles different movement distances.
