# Coordinate Semantics

The race uses the turtle graphics coordinate system for both placement and finish detection.

- The screen is configured to 800 by 400 pixels.
- Each turtle starts at `x=-370`.
- The six starting y-values are `-70`, `-40`, `-10`, `20`, `50`, and `80`.
- During the race, the code checks whether a turtle's x-coordinate is greater than `370`.

The source does not draw a separate finish-line object. The `370` value is a logical threshold used by the race loop.
