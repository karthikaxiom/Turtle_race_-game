# Inner Loop Continuation

Changing `race_on` to `False` affects the next evaluation of the outer `while` condition; it does not cancel the already-running `for turtle_ in all_turtles` traversal. Remaining entries in the current pass still reach their normal check and movement call.

The canonical explanation is [Race Termination](RACE_TERMINATION.md), which also describes the possibility of multiple result messages in one pass.
