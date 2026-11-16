# Finish Detection During a Pass

A successful finish check sets `race_on` to false and prints a result, but the source contains no `break` from the active `for` loop.

Therefore:
- the turtle that triggered the check still reaches its movement call;
- later turtles in the same list pass are still checked and moved;
- a later turtle can also satisfy the threshold and print another result;
- the outer `while` loop does not begin another pass after the current pass completes.

This is why “first detected” means first qualifying turtle in the current traversal, not necessarily the only result printed during that pass. See [Race Termination](RACE_TERMINATION.md) and [Inner Loop Continuation](INNER_LOOP_CONTINUATION.md).

## Interpretation example

Suppose an early list entry is already beyond the threshold when checked. Its result is printed and the flag becomes false, but its movement call still runs. If a later entry is also beyond the threshold when its turn arrives, that entry can print another result. The later message may therefore be the last visible result from that pass; this is a consequence of list traversal, not a tie-breaking feature.
