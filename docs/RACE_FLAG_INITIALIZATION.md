# Race Flag Initialization

The race loop is controlled by `race_on`.

It is initialized from the user's input: a non-empty response starts the race, while a missing response leaves the race disabled. Once initialized, the value is used directly by the outer `while` loop to decide whether race iterations should run.
