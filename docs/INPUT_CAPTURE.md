# Input Capture

`screen.textinput(...)` runs after screen configuration and before turtle creation. Its return value is assigned to `user_bet`.

The stored value has two later uses:
- Its truthiness initializes `race_on` after all six turtles have been configured.
- Its lowercase form is used in the result comparison if a finish condition is detected.

The source does not trim or validate the value at capture time. See [Initialization Sequence](INITIALIZATION_SEQUENCE.md), [Input Lifecycle](INPUT_LIFECYCLE.md), and [Input Normalization Boundary](INPUT_NORMALIZATION_BOUNDARY.md).