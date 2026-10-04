# Turtle Placement

Each turtle is positioned with `goto()` during initialization.

The x-coordinate is fixed at `-370`, while the y-coordinate comes from the indexed `y_positions` list. The same index is used to select the turtle color and its vertical position.

Placement occurs after `penup()`, so initialization moves the turtle without drawing a trail.