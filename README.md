# Turtle Race Game 🐢

A small Python `turtle` graphics game where six colored turtles race across the screen. Choose a turtle color before the race starts, then see whether your pick reaches the finish first.

## Features

- Six turtles: red, orange, yellow, green, blue, and purple
- A pre-race color bet entered through a `turtle` text-input dialog
- Random movement on every loop, giving each race a different outcome
- A terminal message showing whether the selected turtle won or lost
- A graphical race window that remains open until clicked after the race

## How the Race Works

The program creates six turtles at fixed vertical positions near the left side of an `800 × 400` window. During the race, each turtle advances by a random integer distance from `0` to `10` pixels per loop. The first turtle whose x-coordinate passes `370` is treated as the winner.

The entered bet is compared case-insensitively with the winning turtle's color before the result is printed.

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
