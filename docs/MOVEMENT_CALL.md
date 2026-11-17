# Movement Call

Each processed turtle receives one `forward(random.randint(0, 10))` call after its finish check. The generated integer is inclusive of both endpoints, so a zero-distance step is possible.

Use [Movement Semantics](MOVEMENT_SEMANTICS.md) as the maintained reference for range, randomness, and per-turn ordering.

## Per-turn call contract

The random expression is evaluated as the argument to `forward(...)`, so a fresh integer is requested for each processed turtle. The call is not skipped merely because the preceding finish check set `race_on` to false; it remains in the current `for` iteration.
