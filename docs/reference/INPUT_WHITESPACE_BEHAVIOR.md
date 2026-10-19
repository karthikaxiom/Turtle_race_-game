# Input whitespace behavior

The result comparison applies `.lower()` to the stored input but does not strip surrounding whitespace. Therefore an otherwise matching color with extra leading or trailing spaces will not compare equal to the winner color.