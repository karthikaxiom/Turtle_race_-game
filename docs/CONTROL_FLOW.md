# Control Flow Boundaries

The script has a linear setup phase, an optional race phase, and a shared shutdown step. There is no separate event-driven winner handler or replay loop.

## 1. Screen and input setup

The screen is created and configured, then the input dialog stores its return value in `user_bet`.

## 2. Participant initialization

The program creates six turtles, configures their color and position, and appends them to `all_turtles`. Only after this setup does it initialize `race_on` from the input's truthiness. A falsey input therefore skips the race phase without skipping participant creation.

## 3. Race processing

The outer `while race_on` loop contains a `for turtle_ in all_turtles` traversal. For each participant, the source checks `xcor() > 370` before calling `forward(random.randint(0, 10))`.

When the check succeeds, `race_on` becomes false and a result is printed. The assignment does not interrupt the active `for` loop: the current turtle still reaches its movement call, and later turtles in that pass continue to be processed. After the pass completes, the outer condition prevents a new pass.

## 4. Shutdown

Both the completed-race path and the falsey-input path reach `screen.exitonclick()`. The window is left open for the user to click; there is no separate restart path in the current script.

Source of truth: `main.py`.
