# Inner Loop Continuation

Setting `race_on` to `False` ends the outer `while` loop after the current pass, but it does not interrupt the active `for turtle_ in all_turtles` iteration.

Remaining turtles in that pass still reach their existing checks and movement calls.