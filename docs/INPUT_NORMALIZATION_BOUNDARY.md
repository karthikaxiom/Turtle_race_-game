# Input Normalization Boundary

The startup dialog returns a value that is stored in `user_bet`. The original value is retained; the program does not normalize it when the dialog closes.

When a detected turtle is compared with the entered guess, the source evaluates:

```python
winning_color == user_bet.lower()
```

Normalization is applied to the user's stored text at the comparison point:

- Letter case is ignored because `lower()` is called on `user_bet`.
- Leading and trailing whitespace is not removed because the code does not call `strip()`.
- No check rejects values outside the six configured color names before the race begins. Any non-empty text enables the race, even when it cannot match a configured turtle color.
- A cancelled or empty input is falsey and leaves `race_on` disabled.

The detected color comes from `turtle_.pencolor()`; the current code does not call `lower()` on that value. The configured colors are already lowercase.

This page describes the current comparison boundary, not a recommendation for input validation. Source of truth: `main.py`.
