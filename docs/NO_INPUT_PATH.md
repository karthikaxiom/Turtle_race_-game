# No-Input Path

When the startup dialog returns a falsey value, turtle setup still completes, `race_on` is initialized to false, and the movement loop is skipped. Execution then reaches the same `screen.exitonclick()` call used after a completed race.

The maintained path description is [Input Lifecycle](INPUT_LIFECYCLE.md); the shared close behavior is in [Screen Shutdown](SCREEN_SHUTDOWN.md).
