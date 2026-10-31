# Loop State Transition

The race loop starts with `race_on` set from the presence of a user input value.

During winner detection, a qualifying turtle changes `race_on` to `False`. The next outer-loop condition then prevents another race pass.