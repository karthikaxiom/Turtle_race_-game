# Output and Environment

## Terminal output

The current implementation prints one of two result formats when a qualifying turtle is detected:

- `You've won! The <color> turtle is the winner!`
- `You've lost! The <color> turtle won.`

The color is taken from the detected turtle's current pen color.

## Graphical runtime

The program uses Python's standard-library `turtle` module for its graphical interface and `random` for movement distances. No third-party Python package is imported by `main.py`.

The graphical window requires a desktop environment capable of opening the turtle window and a Python installation with the Tk support needed by `turtle`.

The script can be launched with a Python 3 command such as `python main.py` or `python3 main.py`, depending on the system.

Because results are printed with `print(...)`, running the script from a terminal is the direct way to observe the win/loss messages.
