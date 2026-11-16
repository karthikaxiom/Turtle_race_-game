# Loop Condition

The outer `while` loop continues only while `race_on` is true. The flag is initialized from the startup input's truthiness and is set to false when a processed turtle is found beyond the logical finish threshold.

See [Race Termination](RACE_TERMINATION.md) for the maintained explanation of both transitions and the current-pass behavior.

## Transition timing

There are two sources of the flag's value: its initial truthiness-based assignment after participant setup, and the finish branch that assigns `False`. There is no assignment that restores it to `True` inside the loop. Consequently, once a finish check clears the flag, another outer pass is not scheduled.
