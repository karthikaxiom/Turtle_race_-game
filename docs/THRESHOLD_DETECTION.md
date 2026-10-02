# Threshold Detection Timing

Winner detection is based on the turtle's x-coordinate at the beginning of its turn.

The condition is:

`turtle_.xcor() > 370`

This has two important consequences.

## Crossing during movement

A turtle can move from a position at or below `370` to a position above `370` during its `forward(...)` call. That movement does not immediately trigger the result branch, because the check for that turtle has already happened for the current turn.

The turtle is detected when it is processed again and its x-coordinate is already above `370`.

## Equality

An x-coordinate of exactly `370` does not satisfy the condition because the comparison uses `>`, not `>=`.

There is no separate finish-line collision or event handler; detection is performed directly inside the race loop.