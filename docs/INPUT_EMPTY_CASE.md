# Empty Input Case

An empty string from the startup dialog is falsey. The program still creates and positions all six turtles, then initializes `race_on` as false. The movement loop is skipped and execution reaches `screen.exitonclick()`.

No result message is printed, no validation error is shown, and the dialog is not reopened. See [Input Lifecycle](INPUT_LIFECYCLE.md) and [Input Cancellation](INPUT_CANCELLATION.md).