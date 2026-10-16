# Result Check Sequence

Winner handling occurs inside the turtle iteration loop.

- The current turtle's x-coordinate is checked first.
- A turtle beyond the `370` threshold is treated as a detected winner.
- The current pen color supplies the winner color for the message.
- The entered bet is compared to that color after converting the bet to lowercase.
- The result is printed before the turtle receives that turn's movement call.

The sequence explains why the finish check and movement call are distinct operations in the current loop.
