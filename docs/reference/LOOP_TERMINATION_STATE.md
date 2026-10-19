# Loop termination state

The race loop is controlled by `race_on`. Once a turtle satisfies the finish condition, `race_on` is set to `False`, allowing the outer `while` loop to terminate after the current pass completes.