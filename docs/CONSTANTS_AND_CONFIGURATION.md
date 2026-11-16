# Constants and Configuration

This page records fixed values in the current `main.py`; none are loaded from a configuration file.

## Window

- Width: `800`
- Height: `400`
- Title: `Turtle Race ` (including the trailing space in the source)

## Participants

The color list is `red`, `orange`, `yellow`, `green`, `blue`, `purple`.

The paired y-coordinate list is `-70`, `-40`, `-10`, `20`, `50`, `80`. Both lists are indexed by the same creation-loop counter, so their order is significant.

## Position and finish

- Starting x-coordinate: `-370` for every turtle.
- Finish comparison: `xcor() > 370`.
- Movement draw: `random.randint(0, 10)`, inclusive.

There is no separately created finish-line object. The threshold is a numeric condition in the loop, not a drawn boundary. See [Coordinate System](COORDINATE_SYSTEM.md), [Color Mapping](COLOR_MAPPING.md), and [Movement Semantics](MOVEMENT_SEMANTICS.md).

## Configuration review notes

The two participant lists are parallel configuration: changing their lengths or order independently can break the intended color-to-lane pairing. The creation loop currently uses `range(6)`, so the six-entry relationship is explicit in the implementation. A future configuration refactor should update the loop and both lists together, then recheck the observable participant order.
