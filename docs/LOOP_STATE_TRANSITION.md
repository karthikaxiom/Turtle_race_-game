# Loop State Transition

The input result initializes `race_on` after all six turtle objects have been created.

During the race, a qualifying coordinate check sets `race_on` to `False`. This state change does not break the inner `for` loop; the remaining turtles in that pass are processed. Once the pass finishes, the outer `while` condition is false and no new pass begins.

A falsey startup input initializes the flag as false, so the race loop is skipped entirely. See [State Transitions](STATE_TRANSITIONS.md), [Input Lifecycle](INPUT_LIFECYCLE.md), and [Race Termination](RACE_TERMINATION.md).
