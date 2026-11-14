# Loop Sequence

The setup loop creates six turtle objects in configured order. It uses a shared index to pair each color with its y-coordinate and appends each object to `all_turtles`.

During the race, an outer `while race_on` loop contains an inner `for` loop that visits the stored turtles in list order. Each turtle's position is checked before its random movement call.

The outer loop does not stop the active inner traversal when the flag changes. The full lifecycle is maintained in [Program Lifecycle](PROGRAM_LIFECYCLE.md); see [Turn Order](TURN_ORDER.md) for per-turtle processing.
