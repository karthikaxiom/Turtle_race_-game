# No Validation Path

The startup flow does not check a non-empty guess against the configured color list. An unsupported non-empty value still enables the race, but cannot equal one of the six configured turtle colors in the result comparison.

The canonical input contract, including case conversion and whitespace behavior, is [Input Normalization Boundary](INPUT_NORMALIZATION_BOUNDARY.md).

## Distinguish three input outcomes

A truthy supported color starts the race and can match after lowercasing. A truthy unsupported string also starts the race but cannot match a configured color. A falsey result skips the race loop after setup. These outcomes arise from truthiness and later equality comparison; there is no separate validation branch.
