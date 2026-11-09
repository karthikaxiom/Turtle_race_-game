# Race Flag Initialization

The race state is initialized from the truthiness of `user_bet` after the turtle objects have been created. A truthy value allows the outer `while` loop to run; a falsey value skips it.

See [Input Lifecycle](INPUT_LIFECYCLE.md) for the startup sequence and [Race Termination](RACE_TERMINATION.md) for the later transition to a false state.