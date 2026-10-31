# Post-Winner Movement

The finish check occurs before the movement call for each turtle. If that check identifies a winner, the same iteration still reaches its existing `forward()` call.

This documents the current ordering rather than proposing a control-flow change.