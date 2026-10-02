# Configuration Constants

This note records the fixed configuration values used by the current implementation in `main.py`.

## Window

- Width: `800`
- Height: `400`
- Title: `Turtle Race `

The window dimensions are supplied directly to `screen.setup(...)`.

## Turtle configuration

The program defines six colors:

`red`, `orange`, `yellow`, `green`, `blue`, and `purple`.

Their starting vertical coordinates are:

`-70`, `-40`, `-10`, `20`, `50`, and `80`.

The two lists are indexed together when the turtle objects are created.

## Race boundary

The current winner check uses an x-coordinate threshold of `370`. There is no separately drawn finish-line object in the implementation.

These values are implementation constants, not values loaded from a configuration file.