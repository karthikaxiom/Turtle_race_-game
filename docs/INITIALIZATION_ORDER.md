# Initialization Order

The current program performs setup in this order:

1. Import turtle and random.
2. Create the turtle screen.
3. Configure the screen size and title.
4. Display the startup text-input dialog.
5. Create the all_turtles list.
6. Create six turtle objects.
7. Assign each color.
8. Lift each pen.
9. Move each turtle to its starting coordinate.
10. Append each turtle to all_turtles.
11. Set race_on from the returned input value.
12. Enter the race loop only when race_on is truthy.

The turtle objects therefore exist before the first while race_on condition is evaluated. A cancelled startup dialog does not skip turtle creation; it leaves the race loop disabled.
