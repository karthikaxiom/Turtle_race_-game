# Finish Boundary Semantics

The finish condition is the strict comparison `turtle_.xcor() > 370`. A turtle at exactly `370` does not satisfy it. The coordinate is checked before that turtle's movement call, so crossing the boundary during movement is detected on a later turn.

Use [Threshold Detection Timing](THRESHOLD_DETECTION.md) as the canonical explanation of the boundary and its timing. This page remains a concise topic entry, not a separate specification.
