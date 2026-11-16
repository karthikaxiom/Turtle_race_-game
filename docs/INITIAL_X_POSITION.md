# Initial Horizontal Position

All six turtle objects are placed at the same horizontal coordinate, x = -370. The creation loop pairs each participant's vertical coordinate with its color by index.

The shared x-coordinate is assigned in `goto(x=-370, y=y_positions[i])` after `penup()`. It is an initial position only; the race loop subsequently changes each turtle's horizontal coordinate through `forward(...)`.

See [Starting Positions](STARTING_POSITIONS.md) and [Coordinate System](COORDINATE_SYSTEM.md).