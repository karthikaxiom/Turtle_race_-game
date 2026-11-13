# Input Lifecycle

The interactive input step occurs after the screen is configured and before the turtle objects are created. `screen.textinput(...)` returns the dialog value, which the script stores in `user_bet`.

## How the value is used

The script does not immediately start moving turtles when the dialog closes. It first creates and configures all six participants. After that, the truthiness of `user_bet` initializes `race_on`:

- A non-empty value enables the outer race loop, even if the text is not one of the configured colors.
- A falsey value leaves the loop disabled. The six turtles still exist, but no movement calls or result messages are produced by the race loop.

If a turtle is later detected beyond the finish threshold, the stored value is used again in the comparison `winning_color == user_bet.lower()`. This lowercases the entered text at comparison time; it does not trim spaces or validate the color at startup.

See [Input Normalization Boundary](INPUT_NORMALIZATION_BOUNDARY.md) for the exact comparison limitations and [Initialization Sequence](INITIALIZATION_SEQUENCE.md) for the full order of operations.
