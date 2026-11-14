# Input and Output Boundaries

The startup dialog returns a value that is stored in `user_bet`. Its truthiness controls whether the race loop begins; the program does not validate the guess against the configured colors before starting.

The win/loss messages are printed to standard output. They are separate from the Turtle graphics window, which displays the participants and remains open for a click at shutdown.

For the detailed paths, see [Input Lifecycle](INPUT_LIFECYCLE.md), [Input Normalization Boundary](INPUT_NORMALIZATION_BOUNDARY.md), [Output and Environment](OUTPUT_AND_ENVIRONMENT.md), and [Screen Shutdown](SCREEN_SHUTDOWN.md).
