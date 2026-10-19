# Cancellation behavior

If the text-input dialog returns no value, `race_on` is initialized to `False`. Turtle creation still occurs because object setup follows the input dialog, but the race loop itself is skipped.