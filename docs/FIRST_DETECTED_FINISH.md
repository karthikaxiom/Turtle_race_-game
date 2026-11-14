# Finish Detection During a Pass

A successful finish check sets `race_on` to false and prints a result, but the source contains no `break` from the active `for` loop.

Therefore:
- the turtle that triggered the check still reaches its movement call;
- later turtles in the same list pass are still checked and moved;
- a later turtle can also satisfy the threshold and print another result;
- the outer `while` loop does not begin another pass after the current pass completes.

This is why “first detected” means first qualifying turtle in the current traversal, not necessarily the only result printed during that pass. See [Race Termination](RACE_TERMINATION.md) and [Inner Loop Continuation](INNER_LOOP_CONTINUATION.md).
