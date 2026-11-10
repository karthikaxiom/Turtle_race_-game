# Movement and Drawing

Each turtle's pen is lifted before initial placement and remains lifted during the race, so `forward(...)` updates position without drawing a trail.

See [Turtle Pen State](../PEN_STATE.md) for pen behavior and [Movement Semantics](../MOVEMENT_SEMANTICS.md) for the random step and per-turn ordering.