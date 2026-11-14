# Data Flow

The current program uses a short in-memory flow. It does not read from a database, file, or network service.

1. `turtle.Screen()` establishes the graphics runtime and the screen is configured.
2. `screen.textinput(...)` returns a value stored in `user_bet`.
3. `colors` and `y_positions` provide paired setup values by index.
4. Each configured turtle reference is appended to `all_turtles`.
5. The race loop reads each object's current x-coordinate.
6. `random.randint(0, 10)` supplies an integer movement distance.
7. `forward(...)` updates the turtle object's position.
8. On a qualifying check, `pencolor()` supplies the displayed winner color.
9. `user_bet.lower()` supplies the comparison value; it does not strip whitespace.
10. `print(...)` sends the result to standard output.
11. `screen.exitonclick()` waits for the final window click.

## Persistence boundary

The input, lists, turtle references, and race flag exist only in the running process. The script does not save a score, movement sequence, random seed, or history between launches.

See [State Variables](STATE_VARIABLES.md), [Input Lifecycle](INPUT_LIFECYCLE.md), and [Output and Environment](OUTPUT_AND_ENVIRONMENT.md).
