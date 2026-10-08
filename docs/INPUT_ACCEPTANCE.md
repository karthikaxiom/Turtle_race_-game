# Input Acceptance

`main.py` stores the value returned by `screen.textinput()` in `user_bet`.

The code does not validate the entered text against the six configured colors before creating the turtles. Any non-empty returned string makes `race_on` true, while a falsey return value leaves `race_on` false.

Later, when a turtle crosses the threshold, the stored input is converted to lowercase for the winner comparison. The conversion does not otherwise alter the original stored value.

Source of truth: `main.py` input capture, race-state initialization, and result comparison.
