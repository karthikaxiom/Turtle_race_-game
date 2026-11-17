# Screen Configuration

The current `main.py` configures the turtle graphics screen before collecting input.

- The screen is created with `turtle.Screen()`.
- The configured width is `800` and the height is `400`.
- The window title is `Turtle Race `.
- No additional screen configuration or external GUI framework is present in the current implementation.

The six turtles are placed relative to this configured screen using an initial x-coordinate of `-370` and explicit y-coordinates.

## Setup order and geometry notes

Screen creation and configuration occur before the text-input dialog. The 800-by-400 dimensions are window settings; they do not themselves create a finish line or enforce a collision boundary. The finish threshold is evaluated separately from screen configuration in the race loop.
