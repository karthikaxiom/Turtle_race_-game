# Movement Semantics

Each active pass iterates through `all_turtles` in list order. For each turtle, the program checks its current x-coordinate and then makes one movement call:

```python
turtle_.forward(random.randint(0, 10))
```

A fresh random integer is drawn for every processed turtle turn. The range is inclusive from 0 through 10, so a zero-distance call is valid and leaves the turtle where it is for that step.

## Ordering and consequences

- The finish check is evaluated before the current turtle's movement call.
- A movement that takes a turtle beyond x = 370 is not detected immediately; the turtle must reach a later turn for the check to observe the new coordinate.
- The movement call still occurs in the current turn when the finish condition has just been detected.
- Changing `race_on` to false does not interrupt the inner `for` traversal; later turtles in that pass still receive their check and movement call.
- There is no explicit sleep or fixed delay in the race loop.
- The source does not seed Python's random-number generator or record the movement draws.

These statements describe the movement mechanism. They do not guarantee that every launch produces a different outcome, identify which turtle will finish first, or specify a completion time. See [Threshold Detection Timing](THRESHOLD_DETECTION.md) and [Race Termination](RACE_TERMINATION.md) for the related control-flow effects.

Source of truth: `main.py` (`random.randint(0, 10)` and `forward()`).
