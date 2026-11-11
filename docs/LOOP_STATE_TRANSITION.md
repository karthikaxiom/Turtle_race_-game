# Loop State Transition

The input result initializes `race_on`; during the race, a qualifying finish check sets it to `False`. The active inner traversal completes, and the outer `while` loop then stops before another pass begins.

See [State Transitions](STATE_TRANSITIONS.md) for the canonical flag lifecycle and [Race Termination](RACE_TERMINATION.md) for loop behavior.
