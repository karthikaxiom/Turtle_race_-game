# Invalid Color Behavior

A non-empty unsupported string is truthy, so it does not prevent the race from starting. Since the final comparison uses the configured winner color, unsupported text will not match one of the six configured color names.

See [Input Normalization Boundary](../INPUT_NORMALIZATION_BOUNDARY.md) for the exact validation and comparison behavior.