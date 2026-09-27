# Input Behavior

The startup input is collected with:

`screen.textinput(title="Make your bet", prompt="Which turtle will win the race? (Enter a color): ")`

The current implementation handles the returned value as follows:

- A cancelled dialog produces a falsey value, so `race_on` becomes false.
- Any non-empty entered string is truthy and therefore starts the race.
- The program does not validate the entered text against the six configured colors before starting.
- When a winner is checked, the entered value is compared with the winner color after calling `user_bet.lower()`.
- Letter case is therefore ignored for a normal string input.
- Leading and trailing whitespace are not removed before the comparison.
- The configured turtle colors are `red`, `orange`, `yellow`, `green`, `blue`, and `purple`.

These behaviors describe the current code; they are not input-validation recommendations.
