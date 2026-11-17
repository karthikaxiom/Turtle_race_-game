# Movement Randomness

The movement distance is drawn with `random.randint(0, 10)` for each processed turtle turn. Both endpoints are included, so no movement is a valid outcome; randomness affects horizontal progress but not the configured turtle color or lane.

The canonical movement explanation is [Movement Semantics](MOVEMENT_SEMANTICS.md).

## What randomness does not change

Random draws affect only the distance passed to `forward(...)`. They do not select a turtle's color, reorder `all_turtles`, change its lane, or alter the finish threshold. The code does not call `random.seed(...)`, so the application does not establish a reproducible movement sequence itself.
