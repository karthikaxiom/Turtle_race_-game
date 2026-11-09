# Race State Lifecycle

The race state has two principal transitions:

1. After turtle setup, `race_on` is initialized from whether `user_bet` is truthy. A cancelled or empty input leaves it false, so the race loop is skipped.
2. During an active race, a turtle whose current x-coordinate is greater than 370 sets `race_on` to false. The current inner-loop pass still completes; no new outer-loop pass begins.

The startup behavior is detailed in [Input Lifecycle](INPUT_LIFECYCLE.md). Finish detection and same-pass processing are detailed in [Race Termination](RACE_TERMINATION.md).

This page summarizes the state transitions; it does not imply a restart or replay control.