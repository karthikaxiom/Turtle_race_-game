# Determinism Boundary

A run contains both fixed configuration and random movement.

## Fixed by the source

- Six turtle objects are created.
- The colors are assigned in the order red, orange, yellow, green, blue, purple.
- The starting x-coordinate is -370 for every turtle.
- The starting y-coordinates are -70, -40, -10, 20, 50, and 80.
- The screen is configured to 800 by 400.
- The turtles are traversed in their list order during each active pass.
- The finish test uses the strict comparison `xcor() > 370`.

## Variable during a run

For each processed turtle turn, the program calls `random.randint(0, 10)` and passes that draw to `forward()`. Each call can return any integer in the inclusive range, including zero. The source does not set an explicit random seed.

The movement sequence therefore depends on the random draws made during execution. The exact finishing order and number of result messages cannot be inferred from the fixed configuration alone.

This does not mean every launch must produce a different outcome. Random runs can coincide, and this page does not promise a particular winner or completion time.

Source of truth: `main.py`.
