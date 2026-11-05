# Observable Behavior Checklist

Use this checklist for a manual review of the current `main.py` behavior. It is not an automated test suite, and race outcomes are not deterministic because movement distances come from `random.randint(0, 10)`.

## Before the race

- [ ] Launch the script from a terminal so that `print(...)` output is visible.
- [ ] Confirm that the graphics window is configured to 800 by 400 before the input dialog appears.
- [ ] Confirm that the input dialog appears before the six turtle objects are created.
- [ ] Confirm that the six turtles are created in the configured color order: red, orange, yellow, green, blue, purple.
- [ ] Confirm that their starting x-coordinate is -370 and their y-coordinates are -70, -40, -10, 20, 50, and 80 in the same order.
- [ ] Confirm that each turtle uses the `turtle` shape and begins with its pen lifted.

## Input paths

- [ ] **Cancel the dialog.** The returned value is falsey, so `race_on` becomes false. The turtle objects are still created, but the movement loop is skipped and no win/loss message is printed.
- [ ] **Enter a supported color in lowercase.** A non-empty value enables the race. When a turtle is detected beyond the threshold, its color is compared with the entered value.
- [ ] **Enter a supported color in uppercase.** The comparison uses `user_bet.lower()`, so letter case alone does not prevent a match.
- [ ] **Enter an unsupported non-empty value.** There is no supported-color validation before the race starts. The race still runs, but the entered value cannot equal one of the six configured turtle colors.
- [ ] **Enter a color with leading or trailing spaces.** The input is lowercased but not stripped, so spaces remain and prevent an otherwise matching color string from comparing equal.

The random race outcome means these checks should verify the input and comparison behavior, not assume which turtle will win or how many result lines will be printed.

## Race loop and finish handling

- [ ] Confirm that each turtle's x-coordinate is checked before that turtle's movement call.
- [ ] Confirm that each movement distance is an integer from 0 through 10, inclusive. A zero-distance movement is valid.
- [ ] Confirm that a turtle moved beyond x = 370 is detected when its next turn reaches the finish check; the code does not check the threshold again immediately after the movement call.
- [ ] Confirm that the inner `for` loop does not break when `race_on` becomes false. Later turtles in the same pass are still checked and moved.
- [ ] Confirm that more than one result line is possible if multiple turtles are already beyond the threshold when their turns are processed in the same pass.
- [ ] Confirm that the outer `while` loop does not start another pass after the current pass completes with `race_on` false.

## Output and shutdown

- [ ] Confirm that result messages are printed in the terminal, not rendered as text inside the turtle window.
- [ ] Confirm that the reported color comes from the detected turtle's current pen color.
- [ ] Confirm that a matching comparison uses the win message and a non-matching comparison uses the loss message.
- [ ] Confirm that `screen.exitonclick()` is reached after either a completed race or a cancelled input dialog, and that the window waits for a click to close.

## Review boundary

These checks describe the behavior present in `main.py`; they do not imply that the repository contains automated tests or that random race outcomes can be reproduced reliably. Treat `main.py` as the source of truth if the implementation changes.
