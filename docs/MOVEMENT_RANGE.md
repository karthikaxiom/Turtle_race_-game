# Random Movement Range

Each turtle receives its movement distance from:

`random.randint(0, 10)`

The generated value is an integer in the inclusive range from `0` through `10`.

## Consequences

- A value of `0` leaves the turtle at its current position for that movement call.
- Values from `1` through `10` advance the turtle forward by that many turtle-coordinate units.
- A new random value is generated separately for each turtle movement call.

The source code does not define a fixed movement distance, speed setting, or explicit timing interval. The movement amount therefore comes directly from the random integer generated for each call.