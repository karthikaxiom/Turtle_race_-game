# Input Lifecycle

The interactive input step occurs after the screen is configured and before the turtle objects are created.

`screen.textinput(...)` returns the value supplied through the dialog. That value is stored in `user_bet` and is then used only to determine whether the race loop starts and to compare the eventual result.

If the dialog returns a falsey value, `race_on` is initialized to `False`, so the movement loop is skipped. The turtle objects have still been created before this state is evaluated.
