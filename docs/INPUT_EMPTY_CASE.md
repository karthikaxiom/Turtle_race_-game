# Empty Input Case

An empty or cancelled dialog result is falsey. Turtle setup still completes, but `race_on` is false when the loop is reached, so no movement or result message occurs.

See [Input Lifecycle](INPUT_LIFECYCLE.md) for the full startup path and [Screen Shutdown](SCREEN_SHUTDOWN.md) for the final click-to-close behavior.
