# State Variables

The current implementation keeps the race state in a small set of local variables.

- `screen`: the turtle graphics screen.
- `colors`: the six configured turtle colors.
- `y_positions`: the six configured starting vertical coordinates.
- `user_bet`: the value returned by the startup text-input dialog.
- `all_turtles`: the list containing the six created turtle objects.
- `race_on`: controls whether the outer race loop continues.
- `winning_color`: assigned when a turtle satisfies the winner threshold.

There is no persistent score, history, database, file-based state, or saved random seed in `main.py`.
