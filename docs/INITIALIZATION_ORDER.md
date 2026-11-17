# Initialization Order

Startup order is observable: the screen is configured first, then the input dialog appears, then the six turtle objects are created and stored. Only after participant setup does the source initialize `race_on` from the truthiness of `user_bet`.

A cancelled dialog therefore does not bypass participant creation. The turtles are still configured, but the race loop is skipped because the flag is false.

The canonical step-by-step sequence is [Initialization Sequence](INITIALIZATION_SEQUENCE.md).

## Why the order matters

Input capture precedes turtle construction, but race enablement follows it. This means the dialog result is already stored while participant objects are still being created, yet it does not control whether those objects are constructed. It controls only whether the subsequent outer race loop is entered.
