# State Model

The program can be understood as a sequence of execution states controlled mainly by the local variable `race_on`. This is a conceptual description of the current script, not a separate state-management implementation.

1. **Screen setup** — the Turtle graphics window is created and configured.
2. **Input capture** — the startup dialog returns a value stored in `user_bet`.
3. **Participant setup** — six turtle objects are created, positioned, and appended to `all_turtles`.
4. **Race enabled or skipped** — the truthiness of `user_bet` initializes `race_on` after participant setup.
5. **Race active** — while the flag is true, the list is traversed and each turtle is checked and moved in sequence.
6. **Stop requested** — a turtle already beyond the strict finish threshold sets `race_on` to false and causes a result message to be printed.
7. **Window wait** — after the active inner pass completes, the script reaches `screen.exitonclick()`.

A falsey input bypasses the active-race state but still passes through participant setup and window wait. The code keeps no persistent score, saved run, or history across launches. See [State Variables](STATE_VARIABLES.md) for the concrete values and [State Transitions](STATE_TRANSITIONS.md) for flag changes.
