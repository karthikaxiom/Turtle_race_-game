# Cancellation Behavior

A falsey result from the startup dialog leaves `race_on` false. Turtle setup still follows the dialog, but the movement loop is skipped.

The maintained startup explanation is [Input Lifecycle](../INPUT_LIFECYCLE.md); the subsequent click-to-close behavior is [Screen Shutdown](../SCREEN_SHUTDOWN.md).