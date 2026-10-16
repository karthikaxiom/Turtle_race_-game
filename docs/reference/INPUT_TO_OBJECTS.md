# Input to Object Creation

The startup input step occurs before the turtle objects are created.

- `screen.textinput(...)` collects the user's initial value.
- The returned value is stored in `user_bet`.
- The six turtle objects are created afterward in the `for` loop.
- Cancelling input does not prevent object creation; it only leaves `race_on` false.

This sequence describes the current execution order without changing the game logic.
