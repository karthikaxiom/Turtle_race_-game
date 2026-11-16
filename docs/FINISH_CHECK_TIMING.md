# Finish Check Timing

At the beginning of each turtle's turn, the loop reads its current x-coordinate and tests the strict threshold before calling `forward(...)`.

A movement step that crosses x = 370 is not detected immediately after that movement. Detection occurs on a later turn for that turtle, when its coordinate is checked again.

The source does not install a continuous collision listener or draw a finish-line object. See [Finish Boundary Semantics](FINISH_BOUNDARY_SEMANTICS.md) and [Turn Sequence](TURN_SEQUENCE.md).