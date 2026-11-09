# Race Enablement Rule

The initial value of `race_on` is derived from whether `user_bet` is truthy. This controls whether the outer race loop is entered after turtle setup.

See [Input Lifecycle](INPUT_LIFECYCLE.md) for the complete startup path and [Race Termination](RACE_TERMINATION.md) for the later false-state transition.