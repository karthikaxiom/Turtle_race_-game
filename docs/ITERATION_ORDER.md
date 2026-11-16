# Iteration Order

The race loop visits turtles in the order they were appended to `all_turtles`: red, orange, yellow, green, blue, purple.

For each turtle, the program checks its current x-coordinate before issuing a random movement call. The order is not randomized between passes.

If a turtle satisfies the finish condition, the outer race flag becomes false, but the remaining entries in that pass are still visited. This can produce more than one result message in a pass. See [Turn Order](TURN_ORDER.md), [Collection Traversal](COLLECTION_TRAVERSAL.md), and [Race Termination](RACE_TERMINATION.md).

## Why order is observable

List order determines the order in which finish checks and result prints occur within a pass. It does not determine which turtle physically reaches the threshold first, because each turtle advances by an independently drawn step on its own turn. Keep these two meanings of order separate when describing a race outcome.
