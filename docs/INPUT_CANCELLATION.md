# Input Cancellation

A cancelled or empty text-input dialog returns a falsey value in the current flow. The script still creates and positions all six turtles, then initializes `race_on` as false.

The movement loop is skipped, no win/loss result is printed, and execution reaches the shared `screen.exitonclick()` call. There is no second prompt or automatic restart.

See [Input Lifecycle](INPUT_LIFECYCLE.md), [No Input Path](NO_INPUT_PATH.md), and [Screen Shutdown](SCREEN_SHUTDOWN.md).