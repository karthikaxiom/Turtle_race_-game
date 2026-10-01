# Rendering and Output Paths

The current implementation has two output paths.

## Graphical path

The turtle module creates the screen and renders the six turtle objects. Movement is performed through the turtle graphics API.

## Terminal path

Race results are emitted with print(...). The result text is not drawn inside the turtle graphics window.

The two paths are used together: the graphics window shows the race, while the terminal receives the detected result message. No separate output file is created by main.py.
