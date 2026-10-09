# Input to Race State

The program uses the value returned by `screen.textinput()` as `user_bet` before creating the turtles. The race state is then initialized from whether that value is truthy: a submitted non-empty string starts the race, while a falsey result leaves `race_on` false. This describes the current control flow without changing the implementation.
