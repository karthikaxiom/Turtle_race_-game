# Random Movement

Each turtle receives a movement distance from Python's `random.randint(0, 10)` during each pass through the race loop.

This means a single movement update can be any integer from `0` through `10`, inclusive. A zero result leaves that turtle's position unchanged for that update.

The random value is generated independently for each turtle update. No random seed is configured in `main.py`, so the source does not prescribe a fixed sequence of movement values.
