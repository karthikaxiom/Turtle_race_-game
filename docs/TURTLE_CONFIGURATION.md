# Turtle Configuration

Each of the six turtle objects is created inside the same initialization loop. The configuration is positional: a single index selects both the turtle's color and its vertical lane.

For every index in `range(6)`, the program:

1. Creates a turtle with `shape="turtle"`.
2. Assigns `colors[i]` with `color(...)`.
3. Calls `penup()` before placement so setup and later forward movement do not draw a trail.
4. Calls `goto(x=-370, y=y_positions[i])` to establish the starting position.
5. Appends the object to `all_turtles`.

The configured color order is red, orange, yellow, green, blue, purple. The corresponding y-coordinate order is `-70, -40, -10, 20, 50, 80`. The same list order is used later by the race loop; the collection is not shuffled for each pass.

The current source creates six participants from the fixed loop bound and does not expose a runtime option to change the count. See [Color Mapping](COLOR_MAPPING.md), [Starting Positions](STARTING_POSITIONS.md), and [Collection Traversal](COLLECTION_TRAVERSAL.md) for the connected contracts.
