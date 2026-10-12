# State Check Before Movement

For each turtle turn, the current x-coordinate is checked before a new random movement distance is generated and applied.

This ordering means the threshold decision uses the position carried into the turn, not the position produced by that same turn's movement call.
