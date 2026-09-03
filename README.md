# Turtle Race Game 🐢

A small Python `turtle` graphics game where six colored turtles race across the screen. Choose a turtle color before the race starts, then see whether your pick is reported among the detected winners.

## Features

- Six turtles: red, orange, yellow, green, blue, and purple
- A pre-race color bet entered through a `turtle` text-input dialog
- Random movement on every loop, giving each race a different outcome
- Terminal result messages showing whether the selected turtle matches each detected winner
- A graphical race window that remains open until clicked after the race

## How the Race Works

The program creates six turtles at fixed vertical positions near the left side of an `800 × 400` window. All six start at x = `-370`; their y-coordinates are paired with the color list in this order: red `-70`, orange `-40`, yellow `-10`, green `20`, blue `50`, and purple `80`.

During the race, each turtle advances by a random integer distance from `0` to `10` pixels per loop. Because `0` is included in that range, a turtle can remain in the same position for a turn. A turtle is recognized as a winner when its x-coordinate is already greater than `370` at the start of its turn in the loop. Because the threshold check happens before that turn's movement, a turtle that first moves from `370` or less to beyond `370` is detected on its next turn through the loop.

The entered bet is compared case-insensitively with the detected winner's color before the result is printed. Because the current implementation checks every turtle in the active pass before the outer race loop stops, more than one result can be printed if multiple turtles have already crossed the threshold by that pass. The movement call also runs after the winner check, so a turtle that is detected beyond the threshold still receives that turn's final random forward movement.

## Controls and Output

- Enter a turtle color in the startup dialog to begin the race.
- Any non-empty text starts the race; the current implementation does not reject unsupported color names, so an unsupported entry cannot match a winning turtle.
- Letter case is ignored when checking the bet because the input is converted with `.lower()`, but leading or trailing spaces are not removed.
- The race itself is automatic; no keyboard controls are required once it starts.
- The result is printed to the terminal as either a win or loss message.
- After the race finishes, click the graphics window to close it.
- Cancelling the startup dialog leaves the race disabled.

## Implementation Notes

- The project uses only Python's standard-library `turtle` and `random` modules.
- Six turtle objects are stored in a list and updated sequentially inside the race loop.
- Starting positions are defined explicitly with matching color and y-position lists.
- Random movement is generated with `random.randint(0, 10)` for each turtle on each loop.
- Winner detection is based on the turtle's x-coordinate crossing the right-side threshold.

## Learning Outcomes

This compact project demonstrates several useful Python fundamentals in one runnable program:

- creating and managing multiple objects in a list
- iterating over objects inside a continuous game loop
- pairing configuration values such as colors and screen positions
- using random values to drive simple simulation behavior
- accepting GUI input and comparing normalized user text
- combining graphical output with terminal feedback

## Project Structure

```text
Turtle_race_-game/
├── main.py      # game setup, betting prompt, race loop, and result handling
└── README.md    # project documentation
```

The repository is intentionally compact: the complete game logic lives in `main.py`, while the README documents setup and behavior.

## Requirements

- Python 3 with Tk support available for the graphical `turtle` window
- No third-party Python packages are imported by `main.py`

## Run Locally

Clone or download the repository, then run:

```bash
python main.py
```

When prompted, enter one of the available colors:

`red` · `orange` · `yellow` · `green` · `blue` · `purple`

If the input dialog is cancelled, the race does not start and the window remains available to close with a click.

## Screenshot

<img width="1011" height="543" alt="Screenshot of the Turtle Race game" src="https://github.com/user-attachments/assets/006caf17-8801-4bd9-900b-620bd7ce7a55" />

## Possible Extensions

- Add a restart control
- Add sound effects
- Track scores across multiple races
- Introduce optional speed-boost mechanics

## License

No license file is currently included in this repository. Unless a license is added, normal copyright rules apply to reuse and redistribution.
