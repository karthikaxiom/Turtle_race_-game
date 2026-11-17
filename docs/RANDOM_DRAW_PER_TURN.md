# Random Draw Per Turn

Each turtle receives one random movement value when its turn is processed. The value is selected from the inclusive range represented by `random.randint(0, 10)`.

Randomness therefore affects movement distance on each processed turn rather than selecting a winner directly.

## Draw timing

The random function is evaluated inside the `forward(...)` argument for each visited turtle. It is not called once per complete round and its value is not shared across participants. A zero draw still counts as a processed movement call, even though the turtle's horizontal position does not advance.
