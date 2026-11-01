# Movement Call Order

For each turtle visited by the race loop, the game checks the turtle's x-coordinate before calling `forward()`.

The random movement therefore affects the turtle after that iteration's finish check. A turtle can cross the finish boundary because of its movement call and is evaluated for winning on the next visit through the loop.