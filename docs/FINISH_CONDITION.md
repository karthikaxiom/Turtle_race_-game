# Finish Condition

For each turtle turn, the program checks whether the turtle's current x-coordinate is strictly greater than `370`:

```python
if turtle_.xcor() > 370:
```

A coordinate equal to `370` does not satisfy this condition. The comparison is performed before the turn's movement call, so a turtle that crosses the threshold during movement is detected on a later visit to that turtle.

When the check succeeds, the program sets `race_on` to false, captures `pencolor()` as `winning_color`, and prints a win/loss message. The subsequent `forward(...)` call still executes during that iteration.

See [Finish Check Timing](FINISH_CHECK_TIMING.md), [Finish Boundary Semantics](FINISH_BOUNDARY_SEMANTICS.md), and [Race Termination](RACE_TERMINATION.md).
