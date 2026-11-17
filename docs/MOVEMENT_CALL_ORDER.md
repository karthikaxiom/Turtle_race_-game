# Movement Call Order

For each turtle, the loop checks `xcor() > 370` before calling `forward(...)`. A movement step can carry a turtle beyond the threshold, but that crossing is detected on a later visit to its turn.

See [Turn Sequence](TURN_SEQUENCE.md) for the maintained operation order and [Threshold Detection Timing](THRESHOLD_DETECTION.md) for the detection boundary.

## Crossing example

If a turtle is checked at x = `369`, it does not meet the strict threshold. If its subsequent step moves it to x = `375`, the program does not immediately re-check it after that call. The next time the loop reaches that turtle's check, the value `375` qualifies. This distinction follows directly from check-before-move ordering.
