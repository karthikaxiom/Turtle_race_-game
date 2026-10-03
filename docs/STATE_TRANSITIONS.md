# Race State Transitions

The race uses the boolean variable `race_on` to control the outer loop.

## Initial state

After the six turtle objects are created, the source assigns:

`race_on = True if user_bet else False`

A truthy input therefore starts the race state as active. A falsey input leaves it inactive.

## Active state

While `race_on` is true, the outer `while` loop processes the turtle list.

## Finish transition

When a processed turtle already has an x-coordinate greater than `370`, the code sets `race_on` to false and records the detected turtle color for result reporting.

The current inner-loop pass still continues through the remaining list entries. Once that pass ends, the false outer-loop condition prevents another pass from starting.