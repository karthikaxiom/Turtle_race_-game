# Input to Race State

The dialog result is stored in `user_bet`. After turtle creation, the source initializes `race_on` from that value's truthiness: a non-empty string enables the race, while a falsey result skips the loop.

See [Input Lifecycle](INPUT_LIFECYCLE.md) for the startup contract and [State Transitions](STATE_TRANSITIONS.md) for the later finish transition.
