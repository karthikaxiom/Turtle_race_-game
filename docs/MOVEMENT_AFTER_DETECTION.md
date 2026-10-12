# Movement After Detection

The finish check occurs before the movement call for each turtle. If the check succeeds, the program still reaches that turtle's `forward()` call before the current loop pass advances.

The movement step therefore remains part of the current turtle turn even when the finish condition has already been detected.
