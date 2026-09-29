# Module Responsibilities

The current implementation imports two Python standard-library modules.

## turtle

main.py uses turtle for the graphical portion of the program, including screen creation, turtle objects, text input, movement, and keeping the window open.

## random

main.py uses random for movement distance through:

```python
random.randint(0, 10)
```

Each movement call obtains an integer from the inclusive range 0 through 10.

No third-party Python package is imported by the current implementation.
