# Input Normalization Boundary

The player's guess is collected as `user_bet` and retained in its entered form until the winner comparison.

The comparison applies `.lower()` to the stored guess, while the winner color comes from `pencolor()`. This means case normalization is performed at the comparison boundary rather than when the input dialog returns.