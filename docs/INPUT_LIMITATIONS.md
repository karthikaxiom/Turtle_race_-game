# Input Limitations

The current source accepts any non-empty text as a truthy startup response. It does not check the entry against the six configured colors before enabling the race.

The comparison later uses `winning_color == user_bet.lower()`. Letter case in the guess is ignored, but leading and trailing spaces are not removed. An unsupported non-empty value can start a full race even though it cannot match a configured color.

The dialog is shown once. There is no validation message, retry prompt, or opportunity to edit the guess during the race.

These are observations about present code, not desired-behavior guarantees. Any validation or retry feature should be labeled a proposal until implemented. See [Input Lifecycle](INPUT_LIFECYCLE.md) and [Input Normalization Boundary](INPUT_NORMALIZATION_BOUNDARY.md).

## Consequences for user experience

Because the dialog is presented only once and no retry branch exists, a mistyped or unsupported non-empty guess is not corrected by the program. The simulation still proceeds. A future validation flow would need to define accepted values, whitespace policy, feedback, and cancellation behavior explicitly; none of those additional steps should be described as current functionality.
