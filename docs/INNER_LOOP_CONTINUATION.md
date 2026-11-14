# Inner Loop Continuation

Changing `race_on` to `False` affects the next evaluation of the outer `while` condition; it does not cancel the active `for turtle_ in all_turtles` traversal.

The turtle that triggers the condition still reaches the movement call that follows the check. Remaining entries in the current pass are also visited, checked, and moved. A later entry can therefore trigger another result message before the pass ends.

Only after the inner traversal completes is the outer condition evaluated again, preventing a new pass. See [Race Termination](RACE_TERMINATION.md) and [Turn Order](TURN_ORDER.md).
