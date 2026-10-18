# Cancelled Input Path

Cancelling the startup dialog produces a falsey input. The turtles are still constructed afterward, but `race_on` remains false, so no race-loop pass executes.
