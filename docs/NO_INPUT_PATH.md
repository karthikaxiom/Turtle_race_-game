# No-Input Path

If the startup dialog returns a falsey value, `race_on` is initialized to false after turtle setup. The movement loop is skipped and no winner message is printed.

See [Input Lifecycle](INPUT_LIFECYCLE.md) for the setup order and [Screen Shutdown](SCREEN_SHUTDOWN.md) for the click-to-close behavior shared by both exit paths.