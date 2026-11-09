# Empty Input Case

An empty or cancelled dialog result is falsey, so the race loop is not entered. The turtles are still created before the loop condition is evaluated.

See [Input Lifecycle](INPUT_LIFECYCLE.md) for the startup sequence and [Screen Shutdown](SCREEN_SHUTDOWN.md) for the shared exit path.