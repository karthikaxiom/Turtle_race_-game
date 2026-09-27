# Execution Flow

The current `main.py` follows this sequence:

1. Import Python's standard `turtle` and `random` modules.
2. Create an `800 × 400` turtle screen and set its title.
3. Show the startup text-input dialog.
4. Create six turtle objects, assign their colors, lift their pens, position them, and store them in `all_turtles`.
5. Set `race_on` from whether the dialog returned a truthy value.
6. While `race_on` is true, visit each turtle in list order.
7. Before each movement, check whether the turtle's x-coordinate is greater than `370`.
8. When a winner is detected, print the corresponding win/loss message and set `race_on` to false.
9. The current turtle still receives its movement call, and later turtles in that same pass are also processed.
10. After the pass finishes, the false `race_on` value prevents another race-loop pass.
11. Call `screen.exitonclick()` so the graphics window remains available for a click.

No persistent state is loaded or saved by this sequence.
