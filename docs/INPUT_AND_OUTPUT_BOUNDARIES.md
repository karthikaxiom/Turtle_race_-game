# Input and Output Boundaries

The project uses two distinct interaction surfaces.

## Input

The turtle graphics module presents the startup text-input dialog. The entered value is kept as text and is used later when comparing the selection with a detected turtle color.

## Output

Race results are sent to the terminal with `print(...)`. The graphics window does not display the win/loss message itself.

The final graphics-window lifecycle is handled separately by `screen.exitonclick()`, so terminal output and window closure are independent parts of the current implementation.
