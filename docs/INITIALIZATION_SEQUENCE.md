# Initialization Sequence

The current `main.py` executes setup in file order:

1. Import `turtle` and `random`.
2. Create the graphics screen; configure width, height, and title.
3. Define the color and vertical-position lists.
4. Display the text-input dialog and store its return value in `user_bet`.
5. Create the empty `all_turtles` list.
6. Iterate over six participant indices.
7. Create each turtle, assign its indexed color, lift its pen, position it at x = -370 and the indexed y-coordinate, then append it.
8. Initialize `race_on` from the truthiness of `user_bet`.
9. Run the nested race loops only while the flag is true.
10. Call `screen.exitonclick()`.

The input dialog precedes turtle creation, but a falsey result does not skip that setup. It only prevents the movement loop from starting. Running the script executes these statements top to bottom.

See [Program Lifecycle](PROGRAM_LIFECYCLE.md) and [Input Lifecycle](INPUT_LIFECYCLE.md).