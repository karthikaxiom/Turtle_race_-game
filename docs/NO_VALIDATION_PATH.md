# No Validation Path

The startup path does not check whether a non-empty entry matches one of the six configured colors. A non-empty unsupported value can therefore start the race, even though it will not match any configured turtle color in the result comparison.

See [Input Normalization Boundary](INPUT_NORMALIZATION_BOUNDARY.md) for the complete comparison behavior and its limitations.