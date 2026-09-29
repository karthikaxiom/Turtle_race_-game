# Turtle Configuration

Each of the six turtle objects is created inside the same initialization loop.

For every index in the configured color and position lists, the program:

1. Creates a turtle with `shape="turtle"`.
2. Assigns the corresponding color with `color(...)`.
3. Calls `penup()`, preventing movement from drawing a trail.
4. Calls `goto(x=-370, y=...)` to establish its starting position.
5. Appends the object to `all_turtles`.

The configured color order is red, orange, yellow, green, blue, purple. The corresponding y-coordinate order is `-70, -40, -10, 20, 50, 80`.
