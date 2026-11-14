# Determinism Boundary

A run combines fixed setup and iteration rules with random movement. Reviewers should distinguish what the source guarantees from what depends on random draws.

## Fixed by the source

- Six turtle objects are created.
- Colors are assigned red, orange, yellow, green, blue, purple.
- All participants start at x = `-370`; y-coordinates are `-70, -40, -10, 20, 50, 80`.
- The screen is 800 by 400.
- Each active pass visits the list in stored order.
- The finish check is the strict comparison `xcor() > 370`, before movement.
- The entered guess is lowercased at comparison time but is not stripped.

## Variable during execution

Each processed turtle turn calls `random.randint(0, 10)`. The range is inclusive, so a call may return zero or ten. The source does not set an explicit seed or store the draws.

Consequently, exact finishing order, number of result messages, and run duration are not fixed by configuration alone. Two runs may still happen to produce the same outcome.

For testing, verify source-defined invariants without asserting a particular winner or elapsed time. See [Observable Behavior Checklist](OBSERVABLE_BEHAVIOR_CHECKLIST.md) and [Movement Semantics](MOVEMENT_SEMANTICS.md).
