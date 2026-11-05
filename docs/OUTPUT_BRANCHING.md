# Output Branching

When a turtle is already beyond the finish threshold at the start of its turn, the program stores its current pen color in `winning_color`:

```python
winning_color = turtle_.pencolor()
```

It then compares that value with `user_bet.lower()`.

- A match prints `You've won! The <color> turtle is the winner!`
- A non-match prints `You've lost! The <color> turtle won.`

The result is sent to standard output with `print(...)`; it is not drawn inside the graphics window. The color in the message is the captured pen color of the turtle that satisfied the check.

Because the inner loop continues after a result is printed, a later turtle in the same pass can also satisfy the threshold and print another result. In that case each qualifying turtle is compared and reported in list order.

Source of truth: `main.py`.
