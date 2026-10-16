# Race State After Input

The `race_on` flag is derived directly from the startup input value.

- A non-empty input value makes `race_on` true.
- A cancelled dialog produces a falsey value, leaving `race_on` false.
- Turtle creation still occurs after this assignment.
- The race loop executes only while `race_on` remains true.
- Once a qualifying turtle sets `race_on` to false, the current inner pass finishes before the outer loop stops.

This reference documents the state transition already implemented in `main.py`.
