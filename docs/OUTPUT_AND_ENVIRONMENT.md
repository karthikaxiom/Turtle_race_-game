# Output and Environment

The game has two separate output surfaces: a Turtle graphics window for the participants and the terminal for result messages. A visible graphics window does not itself display the text printed by the program.

## Terminal output

When a turtle satisfies the finish check, the program obtains its current pen color and prints one of these formats:

- `You've won! The <color> turtle is the winner!`
- `You've lost! The <color> turtle won.`

The comparison is between the captured color and `user_bet.lower()`. These messages are sent through `print(...)`; they are not drawn inside the graphics window. Launch the script from a terminal when you need to observe standard output. Starting it through a file manager may not leave an obvious terminal window visible.

The program does not write a result log, export a report, or save a race history. A falsey input skips the result branch entirely, so no win/loss message is printed for that path.

## Graphical runtime

The program uses Python's standard-library `turtle` module for its screen, input dialog, and turtle objects. The `random` module supplies movement distances. No third-party package is imported by `main.py`.

The Turtle graphics window requires a desktop environment and the Tk support used by Python's `turtle` module. A headless terminal without a graphical display cannot show the race window. The script can be launched with `python main.py` or `python3 main.py`, depending on the Python command configured on the system.

This page describes output and runtime requirements visible in the current source; it does not claim support for a browser interface, a headless rendering mode, or persistent logging. See [Runtime Dependencies](RUNTIME_DEPENDENCIES.md) for the module boundary and [Screen Shutdown](SCREEN_SHUTDOWN.md) for the final window behavior.
