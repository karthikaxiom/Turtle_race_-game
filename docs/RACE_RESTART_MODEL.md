# Race Restart Model

The current program performs one race per launch. The startup path collects the input, creates the turtles, runs the race loop, reports the result, and then waits for the window to close. A new race therefore begins by launching the program again rather than by resetting the existing turtle objects.