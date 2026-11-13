# Threshold Detection Timing

Winner detection is based on the turtle's current x-coordinate at the beginning of its turn. The condition in the source is:

```python
turtle_.xcor() > 370
```

## Crossing during movement

The check runs before `forward(random.randint(0, 10))`. A turtle can therefore move from a position at or below `370` to a position above `370` without being detected during that same check. It is detected when its next turn reaches the condition and the coordinate is already above the threshold.

## Equality and overshoot

An x-coordinate of exactly `370` does not satisfy the condition because the comparison uses `>`, not `>=`. The random movement step can carry a turtle past the threshold without landing exactly on it; the code tests the resulting coordinate on the next visit rather than testing for an exact landing.

## Detection is loop-driven

There is no separate finish-line object, collision callback, or immediate post-movement check. Detection occurs only when the loop processes a turtle and evaluates its current coordinate. See [Race Termination](RACE_TERMINATION.md) for what happens when the condition succeeds during a pass.
