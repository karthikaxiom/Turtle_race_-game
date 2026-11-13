# Determinism Boundary

A run contains fixed configuration and random movement. The distinction matters when reviewing behavior: setup values and loop order can be checked directly, while a particular finishing order cannot be inferred from those values alone.

## Fixed by the source

- Six turtle objects are created.
- Colors are assigned in the order red, orange, yellow, green, blue, purple.
- The starting x-coordinate is `-370` for every turtle.
- Starting y-coordinates are `-70, -40, -10, 20, 50, 80`.
- The screen is configured to 800 by 400.
- Turtles are traversed in their list order during each active pass.
- The finish test uses the strict comparison `xcor() > 370`.
- The input is lowercased only at comparison time; it is not stripped.

## Variable during a run

For each processed turtle turn, the program calls `random.randint(0, 10)` and passes that draw to `forward()`. Each call can return any integer in the inclusive range, including zero. The source does not set an explicit random seed or store a sequence of draws.

The movement sequence therefore depends on the random values produced during execution. Exact finishing order, number of printed result lines, and completion time cannot be derived from the fixed setup alone. This does not mean every launch must produce a different outcome; random runs can coincide.

For manual review, verify fixed configuration and control-flow rules without asserting a specific winner or timing. See [Observable Behavior Checklist](OBSERVABLE_BEHAVIOR_CHECKLIST.md) for practical checks and [Movement Semantics](MOVEMENT_SEMANTICS.md) for the movement call itself.

Source of truth: `main.py`.
