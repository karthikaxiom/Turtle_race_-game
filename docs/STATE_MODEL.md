# State Model

The program can be viewed as a short sequence of states:

1. **Screen setup** — the Turtle graphics window is configured.
2. **Input capture** — the optional color guess is requested.
3. **Participant setup** — six turtle objects are created and positioned.
4. **Race active** — turtles are processed repeatedly while `race_on` is true.
5. **Race finished** — a turtle reaching the logical finish threshold ends the loop and supplies the result.
6. **Window wait** — the program waits for the user to close the graphics window.

This is a behavioral description of the existing control flow, not a new state-management implementation.
