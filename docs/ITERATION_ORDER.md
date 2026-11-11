# Iteration Order

The race loop visits turtles in the order they were appended to `all_turtles`. For each turtle, it checks the current x-coordinate before issuing a random movement call.

See [Turn Order](TURN_ORDER.md) for the maintained per-pass ordering and its effect when the race flag changes during a pass.
