# Observable Behavior Checklist

Use this checklist for a manual review of the current `main.py` behavior. It is not an automated test suite. Race outcomes are non-deterministic because movement distances come from `random.randint(0, 10)`.

## Before the race

- [ ] Launch the script from a terminal so that `print(...)` output is visible.
- [ ] Confirm that the graphics window is configured to 800 by 400 before the input dialog appears.
- [ ] Confirm that the input dialog appears before the six turtle objects are created.
- [ ] Confirm that the six turtles are created in this color order: red, orange, yellow, green, blue, purple.
- [ ] Confirm that their starting x-coordinate is `-370` and their y-coordinates are `-70, -40, -10, 20, 50, 80` in the same order.
- [ ] Confirm that each turtle uses the `turtle` shape and begins with its pen lifted.

## Input paths

- [ ] **Cancel or submit an empty value.** The falsey result leaves `race_on` false. The six turtle objects are still created, the movement loop is skipped, and no win/loss message is printed.
- [ ] **Enter a supported color in lowercase.** A non-empty value enables the race; a matching detected color selects the win branch.
- [ ] **Enter a supported color in uppercase.** The comparison lowercases `user_bet`, so case alone does not prevent a match.
- [ ] **Enter an unsupported non-empty value.** No supported-color validation runs before the race starts; the value cannot equal one of the configured turtle colors.
- [ ] **Enter a color with leading or trailing spaces.** The input is lowercased but not stripped, so the spaces remain and prevent an otherwise matching string from comparing equal.

## Race loop and finish handling

- [ ] Confirm that each turtle's x-coordinate is checked before its movement call.
- [ ] Confirm that each movement distance is an integer from 0 through 10, inclusive. A zero-distance movement is valid.
- [ ] Confirm that a turtle moved beyond x = `370` is detected when its next turn reaches the finish check; the code does not check the threshold again immediately after its movement call.
- [ ] Confirm that exactly x = `370` does not satisfy the strict `>` condition.
- [ ] Confirm that the inner `for` loop does not break when `race_on` becomes false. Later turtles in the same pass are still checked and moved.
- [ ] Confirm that more than one result line is possible if multiple turtles are already beyond the threshold when their turns are processed in the same pass.
- [ ] Confirm that the outer `while` loop does not start another pass after the current pass completes with `race_on` false.

## Output and shutdown

- [ ] Confirm that result messages are printed in the terminal, not rendered inside the turtle window.
- [ ] Confirm that the reported color comes from the detected turtle's current pen color.
- [ ] Confirm that the comparison uses `winning_color == user_bet.lower()`.
- [ ] Confirm that `screen.exitonclick()` is reached after either a completed race or a falsey startup input, and that the window waits for a click to close.

## Review boundary

Perform these checks against the source version being reviewed. Do not infer an automated test pass from a manual run, and do not assume a particular winner, number of result lines, or finish time. If the implementation changes, revise the checklist and the canonical behavior pages together.
