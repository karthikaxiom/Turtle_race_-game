# Output and Environment

The game has two separate output surfaces: a Turtle graphics window for the participants and the terminal for result messages. A visible graphics window does not itself display the text printed by the program.

## Terminal output

When a turtle satisfies the finish check, the program obtains its current pen color and prints one of these formats:

- `You've won! The <color> turtle is the winner!`
- `You've lost! The <color> turtle won.`

The comparison is between the captured color and `user_bet.lower()`. These messages are sent through `print(...)`; they are not drawn inside the graphics window. Launch from a terminal when you need to observe standard output.

The program does not write a result log, export a report, or save race history. A falsey input skips the result branch, so no win/loss message is printed for that path.

## Graphical runtime

The program uses Python's standard-library `turtle` module for its screen, input dialog, and turtle objects. The `random` module supplies movement distances. No third-party package is imported by `main.py`.

The Turtle graphics window requires a desktop environment and the Tk support used by Python's `turtle` module. A headless terminal without a graphical display cannot show the race window. This page does not claim support for a browser interface, headless rendering, or persistent logging.

See [Runtime Dependencies](RUNTIME_DEPENDENCIES.md) and [Screen Shutdown](SCREEN_SHUTDOWN.md).
