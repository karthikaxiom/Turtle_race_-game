# Text Input Storage

The color entered through the `textinput` dialog is stored in `user_bet` before turtle objects are created.

The stored value is later compared with the detected winner after converting the winner color to lowercase. The original input itself is not stripped or otherwise normalized before the comparison.
