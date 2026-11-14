# Console Result Scope

The win/loss result is emitted with `print(...)` when a turtle satisfies the finish check. The message uses the detected turtle's current pen color and compares it with `user_bet.lower()`.

## Terminal behavior

- A matching color produces the win message.
- A non-matching value produces the loss message.
- No result message is printed on the falsey-input path because the race loop is skipped.
- More than one message can be printed in a single pass if later turtles also satisfy the check.

The text is standard output; it is not rendered inside the Turtle graphics window. The program does not save a result log or race history. See [Output and Environment](OUTPUT_AND_ENVIRONMENT.md) and [Race Termination](RACE_TERMINATION.md).
