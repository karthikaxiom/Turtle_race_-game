# Input Acceptance

A truthy dialog result enables the race, but the current program does not validate that a non-empty entry matches one of the six configured colors.

The result comparison is `winning_color == user_bet.lower()`. Letter case in the guess is therefore ignored, but leading and trailing spaces are not removed. An unsupported non-empty value can start a full race and will not match any configured turtle color.

This page describes existing behavior, not an endorsement of the missing validation. See [Input Lifecycle](INPUT_LIFECYCLE.md) for activation and [Input Normalization Boundary](INPUT_NORMALIZATION_BOUNDARY.md) for comparison details.

## Acceptance is separate from matching

The race-enable decision and the later win comparison are separate operations. Truthiness determines whether the loop starts; membership in `colors` is never checked. Thus an unsupported but non-empty guess still enables movement, while the eventual comparison simply follows the ordinary loss branch for each detected turtle.
