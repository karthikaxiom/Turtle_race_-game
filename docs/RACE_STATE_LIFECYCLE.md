# Race State Lifecycle

The race state starts disabled until the startup input is evaluated. A truthy input enables the movement loop. When a participant reaches the finish boundary, the state is disabled and the winner is reported. The lifecycle then proceeds to the existing window-exit behavior.