# Finish Threshold Check

The implementation currently uses `turtle_.xcor() > 370` before that turtle's movement call. The comparison is strict: an x-coordinate equal to `370` is not a finish detection.

See [Threshold Detection Timing](THRESHOLD_DETECTION.md) for the canonical boundary, equality, and next-turn explanation.
