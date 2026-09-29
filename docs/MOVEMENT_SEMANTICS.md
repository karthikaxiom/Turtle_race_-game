# Movement Semantics

Movement is generated independently for each turtle during each active inner-loop pass.

The current implementation calls:

`turtle_.forward(random.randint(0, 10))`

This means the distance is an integer from `0` through `10`, inclusive.

Important consequences of the current implementation:

- A distance of `0` leaves the turtle at its current position for that movement call.
- Each turtle receives its own random draw.
- The movement call occurs after the winner-threshold check for that turtle.
- There is no explicit sleep or fixed delay in the race loop.
- The program does not seed Python's random-number generator, so no explicit deterministic seed is configured.

These notes describe implementation behavior, not a claim that every run produces a different outcome.
