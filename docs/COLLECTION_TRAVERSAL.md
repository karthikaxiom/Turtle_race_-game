# Collection Traversal

The race uses `all_turtles` as its single in-memory collection of participant objects. The creation loop appends each configured turtle once, and the race loop traverses that same list directly:

```python
for turtle_ in all_turtles:
    ...
```

The list order is the creation order: red, orange, yellow, green, blue, purple. It is derived from the common index used with `colors` and `y_positions`.

## Per-pass behavior

Each active outer-loop pass visits every list entry in order. For a visited turtle, the program checks its x-coordinate before making the random movement call. The current implementation does not sort, shuffle, reverse, filter, or rebuild the list during a race.

When one turtle sets `race_on` to false, Python does not stop the already-running `for` traversal. Later entries in the same pass are still visited before the outer condition is evaluated again. This ordering is important to understanding why multiple result messages may appear in one pass; see [Race Termination](RACE_TERMINATION.md).
