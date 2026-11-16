# Race Coordinates

The current implementation uses Turtle coordinates for setup and finish detection. These are logical coordinates, not separate pixel measurements or a drawn track.

## Screen and placement

The screen is configured to 800 by 400. Every turtle starts at x = `-370`; the y-coordinates in participant order are `[-70, -40, -10, 20, 50, 80]`. The shared loop index pairs each y-coordinate with its color. `penup()` is called before `goto()`, so setup does not draw a trail.

## Finish threshold

The race loop tests `xcor() > 370`. Equality does not qualify. There is no separate finish-line object; 370 is a numeric condition evaluated at the start of each turtle's turn.

If movement takes a turtle beyond 370, the crossing is observed on a later visit to that turtle, before its next movement call. See [Finish Check Timing](FINISH_CHECK_TIMING.md) and [Starting Positions](STARTING_POSITIONS.md).