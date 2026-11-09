# Input Cancellation

A cancelled or empty startup dialog follows the falsey-input path: the turtle objects are created, but `race_on` is false and the race loop is skipped.

The full ordering and the subsequent window-exit behavior are maintained in [Input Lifecycle](INPUT_LIFECYCLE.md) and [Screen Shutdown](SCREEN_SHUTDOWN.md).