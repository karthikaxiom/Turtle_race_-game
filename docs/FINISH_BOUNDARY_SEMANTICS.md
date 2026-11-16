# Finish Boundary Semantics

The finish condition is the strict comparison `turtle_.xcor() > 370`. A turtle at exactly 370 does not qualify.

The check runs before that turtle's movement call. If a call moves a turtle from 369 to 374, that turn does not detect the finish; the new coordinate is observed when the turtle is visited again.

This is a logical threshold, not a drawn line or collision event. See [Finish Check Timing](FINISH_CHECK_TIMING.md) and [Race Termination](RACE_TERMINATION.md).