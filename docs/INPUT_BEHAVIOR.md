# Input Behavior

The startup dialog is shown once before turtle creation. Its return value is stored without trimming or validating it against the configured colors.

- A falsey return value skips the race loop after participant creation.
- A truthy return value enables the race.
- The entered value is lowercased only when compared with the detected turtle color.
- Leading and trailing whitespace is preserved.
- There is no retry prompt or mid-race input change.

The canonical detailed references are [Input Lifecycle](INPUT_LIFECYCLE.md) and [Input Normalization Boundary](INPUT_NORMALIZATION_BOUNDARY.md). This file remains a stable entry point for existing links.
