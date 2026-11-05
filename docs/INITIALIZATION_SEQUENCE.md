# Initialization Sequence

`main.py` executes its setup stages in file order:

1. Import the standard-library `turtle` and `random` modules.
2. Create the graphics screen and configure its dimensions and title.
3. Define the color list and the matching vertical-position list.
4. Display the startup text-input dialog and store its return value in `user_bet`.
5. Create the empty `all_turtles` collection.
6. Iterate through six participant indices.
7. For each index, create a turtle with the `turtle` shape, assign the indexed color, lift its pen, move it to x = `-370` and the indexed y-coordinate, then append it to `all_turtles`.
8. Initialize `race_on` from whether `user_bet` is truthy.
9. Execute the race loop only while `race_on` remains true.
10. Call `screen.exitonclick()` after the loop ends.

The input dialog appears before turtle creation, but cancellation does not skip participant setup. All six turtle objects are still created; a falsey input simply leaves `race_on` false, so the movement loop is skipped.

There is no separate application entry-point function. Launching the script executes these stages from top to bottom.

Source of truth: `main.py`.
