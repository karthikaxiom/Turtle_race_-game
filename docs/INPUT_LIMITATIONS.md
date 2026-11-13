# Input Limitations

The current source accepts any non-empty text as a truthy startup response. It does not check the entry against the six configured colors before enabling the race.

The comparison later uses `winning_color == user_bet.lower()`. As a result, letter case in the guess is ignored, but leading and trailing spaces are not removed. An unsupported non-empty value can start a full race even though it cannot match one of the configured colors.

The current input flow also has no retry prompt, validation message, or second chance to edit the guess during a race. The dialog is shown once during startup; see [Input Lifecycle](INPUT_LIFECYCLE.md) for the order and [Input Normalization Boundary](INPUT_NORMALIZATION_BOUNDARY.md) for the exact expression.

These are observations about the present code, not a statement that the limitations are desired product behavior. Any proposed validation or retry feature should be documented as a proposal until implemented.
