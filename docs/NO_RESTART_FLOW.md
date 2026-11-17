# No-Restart Flow

A script launch presents one startup dialog and runs at most one race loop. After `race_on` becomes false, the current inner pass ends, the outer loop is not entered again, and execution proceeds to `screen.exitonclick()`.

See [Program Lifecycle](PROGRAM_LIFECYCLE.md) for the complete launch sequence and [Race Termination](RACE_TERMINATION.md) for the loop exit details.

## Relaunch boundary

The final click closes the current graphics interaction; it does not reinitialize the program state. A new guess and a new set of turtle objects are obtained only by starting a fresh process. There is no in-window button or loop that begins another round.
