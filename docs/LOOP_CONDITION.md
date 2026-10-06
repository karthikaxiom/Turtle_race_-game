# Loop Condition

The outer `while` loop continues only while `race_on` is truthy.

`race_on` is initialized from the input result: a supplied value starts the race, while a cancelled or empty input leaves the race disabled. The loop is later set to false when a turtle is detected beyond the logical right-side threshold.
