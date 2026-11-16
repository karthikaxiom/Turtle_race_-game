# Input Dialog Stage

The dialog is displayed after the graphics screen is configured and before any turtle objects are created. Its return value is stored in `user_bet`.

The prompt requests a turtle color, but the source does not validate the response at this stage. The value is later used for truthiness-based race activation and winner comparison.

See [Initialization Sequence](INITIALIZATION_SEQUENCE.md) and [Input Lifecycle](INPUT_LIFECYCLE.md).