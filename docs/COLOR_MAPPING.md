# Turtle Color Mapping

The `colors` list in `main.py` defines the six turtle colors in this exact order:

1. red
2. orange
3. yellow
4. green
5. blue
6. purple

The turtle-creation loop uses the same index for the color and vertical-position lists. For each index `i`, `new_turtle.color(colors[i])` assigns the corresponding color to the turtle created for `y_positions[i]`.

This indexed pairing keeps lane assignment and color assignment aligned. The order is fixed by the source; only the movement distances are randomized during a race.

Source of truth: `main.py` (`colors`, `y_positions`, and the turtle-creation loop). See [Race Coordinates](COORDINATE_SYSTEM.md) for the associated lane positions.
