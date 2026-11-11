# Movement After Detection

The finish condition is checked before the current turtle's `forward(...)` call. Even when that check succeeds and `race_on` becomes false, the current turtle still reaches its movement call and the remaining turtles in the same pass are processed.

The maintained explanation is [Race Termination](RACE_TERMINATION.md), supported by the per-turtle sequence in [Turn Sequence](TURN_SEQUENCE.md).
