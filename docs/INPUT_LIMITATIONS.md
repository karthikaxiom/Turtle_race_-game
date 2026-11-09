# Input Limitations

The current source accepts any non-empty text as a truthy startup response; it does not validate the value against the configured colors before starting the race.

The exact comparison, lowercasing, and whitespace limitations are maintained in [Input Normalization Boundary](INPUT_NORMALIZATION_BOUNDARY.md). The effect of an empty or cancelled response is maintained in [Input Lifecycle](INPUT_LIFECYCLE.md).