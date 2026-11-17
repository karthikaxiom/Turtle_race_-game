# Race Output

When the race ends, the program reports the color associated with the turtle that crossed the finish threshold.

The result is printed to the terminal before the program waits for the graphics window to be closed.

## Exact reporting behavior

The two message templates are `You've won! The <color> turtle is the winner!` and `You've lost! The <color> turtle won.` The color placeholder is populated from `turtle_.pencolor()` for the turtle currently being checked. Since the active list pass continues after a detection, more than one message can be printed before the window waits for a click.
