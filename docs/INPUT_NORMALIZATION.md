# Input Normalization

The complete input comparison behavior is maintained in [Input Normalization Boundary](INPUT_NORMALIZATION_BOUNDARY.md).

The canonical page documents the exact comparison expression, lowercasing of the user's input, the absence of whitespace trimming, unsupported non-empty values, and the cancelled-input path.

## Transformation actually performed

The source applies one transformation at the point of comparison: `user_bet.lower()`. It does not normalize surrounding whitespace, reject unknown names, or map aliases such as abbreviations to configured colors. Keep the distinction clear: case folding is present; general input sanitization is not.
