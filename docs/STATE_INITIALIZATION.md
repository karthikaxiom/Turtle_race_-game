# State Initialization

The race state is initialized after the turtle collection has been built.

`race_on` is derived from whether the input dialog returned a truthy value. A truthy input starts the race loop; a falsey result leaves the loop disabled.

The turtle collection itself is initialized as an empty list before the creation loop. Each newly created turtle is appended to that list before the race state is evaluated.