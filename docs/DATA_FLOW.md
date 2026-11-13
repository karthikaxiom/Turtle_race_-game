# Data Flow

The current program passes configuration and runtime values through a short, in-memory sequence. It does not use a database, file, or network data flow.

1. `turtle.Screen()` establishes the graphical runtime, after which the script configures the window.
2. The text-input dialog returns a value stored in `user_bet`.
3. The `colors` and `y_positions` lists provide paired setup values for each participant index.
4. Each configured turtle object is appended to `all_turtles`.
5. The race loop reads each object's current x-coordinate before movement.
6. `random.randint(0, 10)` supplies the distance for that turn.
7. `forward(...)` updates the turtle object's position in the graphics runtime.
8. When a threshold check succeeds, `pencolor()` supplies the displayed winner color and `user_bet.lower()` supplies the comparison value.
9. `print(...)` sends the selected result message to standard output.
10. `screen.exitonclick()` handles the final window interaction.

## Value lifetime

The input, configuration lists, turtle collection, and race flag live in the running script's process. The source does not write them to persistent storage or retain a score/history between launches. The random module is called as needed; the script does not save a seed or a sequence of movement draws.

See [State Variables](STATE_VARIABLES.md) for the named variables and [Input Lifecycle](INPUT_LIFECYCLE.md) for the input branch.
