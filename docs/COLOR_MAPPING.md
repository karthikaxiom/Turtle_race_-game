# Turtle Color Mapping

The `colors` list in `main.py` defines the six turtle colors in this exact order:

1. red
2. orange
3. yellow
4. green
5. blue
6. purple

The turtle-creation loop uses the same index for the color and vertical-position lists. Each index assigns one fixed color to the turtle created for the corresponding `y_positions[i]` value.

| Participant index | Color | Starting y-coordinate |
| ---: | --- | ---: |
| 0 | red | -70 |
| 1 | orange | -40 |
| 2 | yellow | -10 |
| 3 | green | 20 |
| 4 | blue | 50 |
| 5 | purple | 80 |

This positional pairing keeps color assignment and lane assignment aligned. The order is fixed by the source; only the movement distances are randomized during a race. See [Starting Positions](STARTING_POSITIONS.md) for placement details and [Collection Traversal](COLLECTION_TRAVERSAL.md) for the order in which the turtles are processed.

Source of truth: `main.py` (`colors`, `y_positions`, and the turtle-creation loop).
