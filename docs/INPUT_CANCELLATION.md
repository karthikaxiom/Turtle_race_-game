# Input Cancellation

The initial bet dialog returns a falsey value when the user cancels it. The program stores that value in `user_bet`, and the race state is then initialized from whether an input value exists.

This means cancellation prevents the race loop from starting rather than producing a normal win or loss result.
