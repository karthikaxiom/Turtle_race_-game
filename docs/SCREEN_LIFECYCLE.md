# Screen Lifecycle

The program creates a Turtle graphics screen before creating the race turtles. The screen is configured with a fixed 800 by 400 window and a title. The same screen remains active while the race loop runs, and `screen.exitonclick()` is called after the race loop ends so the graphics window can remain available until a click closes it.

This document describes the existing program flow only; it does not change the implementation.
