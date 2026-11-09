# Input to Race State

The startup input is stored in `user_bet`; after turtle creation, its truthiness initializes `race_on`. A falsey result skips the movement loop, while a non-empty string enables it.

The maintained sequence is [Input Lifecycle](INPUT_LIFECYCLE.md). The later transition to a stopped race state is covered by [Race Termination](RACE_TERMINATION.md).