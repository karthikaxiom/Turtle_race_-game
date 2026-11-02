# Post-Finish Movement

Winner detection runs before the movement call for the current turtle. If that turtle crosses the threshold, `race_on` is set to false and the result is printed, but the same iteration still reaches `turtle_.forward(...)`.

The outer loop stops only after the current inner-loop pass completes.
