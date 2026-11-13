# State Variables

The current implementation keeps its configuration and race state in local variables within one script execution.

| Name | Role | When it is used |
| --- | --- | --- |
| `screen` | Turtle graphics screen object | Setup and final window interaction |
| `colors` | Ordered participant color configuration | Turtle creation |
| `y_positions` | Ordered starting lane coordinates | Turtle creation |
| `user_bet` | Value returned by the startup dialog | Race activation and result comparison |
| `all_turtles` | Ordered collection of created turtle objects | Race traversal |
| `race_on` | Boolean loop-continuation flag | Outer race loop |
| `winning_color` | Color captured from a turtle that passes the finish check | Result message selection |

## State lifetime

These names are initialized and used in a single process. The source does not save a score, race history, selected guess, random seed, or turtle positions to a file or database. A new script launch creates a new set of objects and requests a new input value.

`winning_color` is assigned when a qualifying turtle is processed. Since the inner loop continues after the first assignment, a later qualifying turtle in the same pass may assign it again before the pass ends. See [Output Branching](OUTPUT_BRANCHING.md) for the observable result behavior.
