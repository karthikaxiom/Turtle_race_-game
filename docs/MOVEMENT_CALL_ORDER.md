# Movement Call Order

For each turtle, the loop checks `xcor() > 370` before calling `forward(...)`. A movement step can carry a turtle beyond the threshold, but that crossing is detected on a later visit to its turn.

See [Turn Sequence](TURN_SEQUENCE.md) for the maintained operation order and [Threshold Detection Timing](THRESHOLD_DETECTION.md) for the detection boundary.
