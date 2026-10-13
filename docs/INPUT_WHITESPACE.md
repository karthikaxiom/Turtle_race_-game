# Input Whitespace

The entered value is passed directly to the result comparison except for the `lower()` call. No `strip()` operation is applied.

Consequently, leading or trailing spaces remain part of the value and can prevent an otherwise matching color name from comparing equal.