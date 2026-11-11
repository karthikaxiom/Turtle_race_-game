# Input Capture

`screen.textinput()` runs after screen configuration and before the turtle creation loop. Its return value is stored in `user_bet`, which is later used both to initialize the race state and to compare the detected turtle color.

See [Initialization Sequence](INITIALIZATION_SEQUENCE.md) for ordering and [Input Lifecycle](INPUT_LIFECYCLE.md) for how the captured value affects execution.
