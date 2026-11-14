# Execution Flow

The current `main.py` follows this order:

1. Import the standard-library `turtle` and `random` modules.
2. Create an 800-by-400 screen and set its title.
3. Display the startup text-input dialog and store its return value.
4. Create six turtle objects; assign color, lift the pen, position each object, and append it to `all_turtles`.
5. Set `race_on` according to the truthiness of the input.
6. While active, traverse the turtle collection in list order.
7. Before moving each turtle, check whether its x-coordinate is greater than `370`.
8. If true, set `race_on` false, capture the pen color, and print the win/loss message.
9. Execute the movement call for the current turtle; continue processing later entries in the same pass.
10. After the pass completes, the false outer-loop condition prevents another pass.
11. Call `screen.exitonclick()`.

The source does not load or save persistent state. This sequence describes the current implementation, not a proposed refactor.
