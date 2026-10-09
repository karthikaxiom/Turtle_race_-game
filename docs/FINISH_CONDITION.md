# Finish Condition

The race loop checks each turtle's x-coordinate against the right-side threshold of `370`. When a turtle is already beyond that threshold at the time of the check, `race_on` is set to false and that turtle's pen color is captured as `winning_color` for the result message.

The movement call still occurs later in the same loop iteration because the `forward()` statement follows the threshold check.
