# Control Flow Boundaries

The program has four main control-flow stages:

## 1. Setup

The screen and its dimensions/title are configured first.

## 2. Input and initialization

The startup text-input dialog runs before turtle objects are created. The six turtles are then initialized and stored in a list.

## 3. Race loop

The outer `while race_on` loop contains a `for turtle_ in all_turtles` loop. Winner detection happens before movement for each turtle.

When a qualifying turtle is found, `race_on` becomes false, but the inner loop is not interrupted. The remaining turtles in that same pass continue through their checks and movement calls.

## 4. Shutdown

Once the current inner pass finishes, the outer loop condition prevents another pass. The program then reaches `screen.exitonclick()`.

This structure means the loop has no explicit `break` statement and no separate restart loop within a single program launch.
