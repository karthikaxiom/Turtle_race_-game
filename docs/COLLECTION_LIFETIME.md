# Turtle Collection Lifetime

`all_turtles` is created as an empty list before turtle objects are constructed.

Each turtle is appended to the list during initialization, and the completed list is then traversed by the race loop. The current program does not replace the list during the race.

The collection therefore serves as the persistent in-memory container for all six turtle objects during one program launch.