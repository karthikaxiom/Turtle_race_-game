# Finish Threshold Check

The implementation uses `turtle_.xcor() > 370` before that turtle's movement call. The comparison is strict: a coordinate equal to 370 is not a finish detection.

When true, the branch sets `race_on` to false, captures the current pen color, and prints a result. The assignment does not interrupt the active inner traversal.

See [Finish Check Timing](FINISH_CHECK_TIMING.md) and [Race Termination](RACE_TERMINATION.md).