# Same-pass behavior after finish

Setting `race_on` to `False` does not immediately break the inner `for` loop. The remaining turtles in that pass can still be processed before control returns to the outer `while` condition.