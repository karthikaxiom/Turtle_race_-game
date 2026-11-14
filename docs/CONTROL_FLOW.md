# Control Flow Boundaries

The script has a setup phase, an optional race phase, and a shared shutdown step. There is no separate event-driven winner handler or replay loop.

## Setup

1. Import `turtle` and `random`.
2. Create and configure the 800-by-400 screen.
3. Collect the user's guess with `screen.textinput(...)`.
4. Create six turtles, configure their colors and positions, and append them to `all_turtles`.
5. Set `race_on` from the truthiness of the input.

A falsey input skips the race phase but does not skip participant creation.

## Race

The outer `while race_on` contains a `for` traversal over the stored turtles. For each turtle, `xcor() > 370` is checked before `forward(random.randint(0, 10))`.

Setting `race_on = False` does not break the active `for` loop. The current turtle reaches its movement call and later entries in that pass are still processed. Only after the pass ends does the outer condition prevent another pass.

## Shutdown

Both paths reach `screen.exitonclick()`. The window waits for a click; the script does not offer a restart control.

Source of truth: `main.py`. See [Program Lifecycle](PROGRAM_LIFECYCLE.md).
