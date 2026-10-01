# Data Flow

The current program passes information through a simple sequence.

1. The screen configuration establishes the graphical runtime.
2. The text-input dialog returns a value stored in user_bet.
3. The color and y-position lists provide configuration for turtle creation.
4. Each configured turtle is stored in all_turtles.
5. The race loop reads each turtle's current x-coordinate.
6. random.randint(0, 10) supplies the movement distance.
7. The turtle object updates its own position through forward(...).
8. A detected winner supplies its current pen color to the result message.
9. screen.exitonclick() handles the final window interaction.

There is no database, file, or network data flow in the current implementation.
