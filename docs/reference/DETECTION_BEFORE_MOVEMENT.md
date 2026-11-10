# Detection Before Movement

The finish check uses the turtle's current x-coordinate before the same turn's random forward movement. A turtle that crosses the threshold during movement is observed on a later finish check.

See [Movement Semantics](../MOVEMENT_SEMANTICS.md) for per-turn ordering and [Race Coordinates](../COORDINATE_SYSTEM.md) for the strict threshold.