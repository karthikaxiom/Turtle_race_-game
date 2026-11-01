# Screen Configuration Boundary

The screen configuration is established before the race input is requested. The current game sets an 800-by-400 window and assigns the title `Turtle Race `.

This makes the display configuration part of startup setup rather than race-loop logic. Later code assumes the screen is already available when it opens the input dialog and creates turtles.