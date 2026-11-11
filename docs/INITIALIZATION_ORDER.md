# Initialization Order

The program's startup order matters: screen setup comes first, the input dialog appears before turtle creation, and `race_on` is initialized only after the six turtles have been configured and stored.

The canonical step-by-step sequence is [Initialization Sequence](INITIALIZATION_SEQUENCE.md). Keep changes to startup ordering there so the lifecycle remains consistent.
