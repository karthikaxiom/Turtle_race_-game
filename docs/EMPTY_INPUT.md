# Empty Input

An empty string returned by the startup dialog is falsey. The program still creates and configures all six turtle objects, then assigns `race_on` a false value and skips the movement loop.

The script proceeds to `screen.exitonclick()`. It does not show a validation error, reopen the dialog, or print a win/loss result for this path.

A cancelled dialog also returns a falsey value in the current Turtle input flow, so it follows the same no-race branch. See [Input Lifecycle](INPUT_LIFECYCLE.md) and [Input Cancellation](INPUT_CANCELLATION.md).
