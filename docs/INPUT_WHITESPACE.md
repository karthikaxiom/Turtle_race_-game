# Input Whitespace

The result comparison lowercases `user_bet` but does not call `strip()`. Leading or trailing spaces therefore remain part of the input and prevent an otherwise matching color name from comparing equal.

The canonical input edge-case reference is [Input Normalization Boundary](INPUT_NORMALIZATION_BOUNDARY.md).

## Concrete comparison examples

| Dialog value | Value after `.lower()` | Can equal a configured color? |
|---|---|---|
| `Red` | `red` | Yes |
| ` red` | ` red` | No |
| `red ` | `red ` | No |
| `RED` | `red` | Yes |

The table assumes the detected turtle color is the canonical lowercase color name. No trimming step occurs between dialog capture and comparison.
