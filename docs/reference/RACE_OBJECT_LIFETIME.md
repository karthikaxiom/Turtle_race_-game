# Race object lifetime

The turtle objects are created once per program launch and retained in `all_turtles` for the duration of that launch. The list is not rebuilt inside the race loop.