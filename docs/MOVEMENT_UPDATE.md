# Movement Update

The race loop calls `forward()` once for each turtle processed in a pass, using a fresh integer from `random.randint(0, 10)`. The distance is inclusive from zero to ten; a zero result leaves that turtle's horizontal position unchanged for that turn.

See [Movement Semantics](MOVEMENT_SEMANTICS.md) for the canonical movement contract and [Turn Sequence](TURN_SEQUENCE.md) for when the call occurs.
