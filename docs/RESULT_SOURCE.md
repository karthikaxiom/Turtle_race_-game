# Result Source

When the threshold condition is satisfied, the program obtains the reported color from:

`turtle_.pencolor()`

The color was previously assigned during turtle creation with:

`new_turtle.color(colors[i])`

Therefore, the reported winner color is taken from the turtle object currently being processed rather than reconstructed from its list index.

The selected input is compared with the detected color after the input is converted with `.lower()`.

The printed result uses the detected turtle color directly in the message. Result reporting therefore depends on the current turtle object's color state and the text returned by the input dialog.