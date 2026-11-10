# Input to Race Flag

The stored dialog result initializes `race_on` by truthiness. A falsey value skips the race loop; a non-empty value enables it after turtle setup.

See [Input Lifecycle](../INPUT_LIFECYCLE.md) for the complete startup path and [Race Termination](../RACE_TERMINATION.md) for the later transition to false.