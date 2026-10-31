# Finish Threshold Check

Winner detection compares the current turtle x-coordinate with the finish boundary before that turtle's movement call.

The current boundary is `xcor() > 370`. Reaching exactly `370` does not satisfy this strict comparison until a later check observes a value above it.