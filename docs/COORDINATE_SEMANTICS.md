# Coordinate Semantics

The canonical coordinate reference is [Coordinate System](COORDINATE_SYSTEM.md). Key distinctions in the current source:

- The screen is configured to 800 by 400.
- Every participant starts at x = `-370`.
- The six y-coordinates are `-70, -40, -10, 20, 50, 80`, paired by list index with the six colors.
- The finish test is strictly `xcor() > 370`; equality does not satisfy it.
- The coordinate is read before the movement call for that turtle's turn.

The numeric threshold is a program condition; the source does not draw a finish-line object. The check is not continuous between loop iterations. See [Finish Check Timing](FINISH_CHECK_TIMING.md).

## Boundary examples

A turtle at x = `370` does not satisfy the strict finish test. A turtle at any x-coordinate greater than `370` does. Because the read occurs before movement, a step that carries a turtle from at-or-below the threshold to beyond it is detected on that turtle's next visit, not by a check immediately after the step.
