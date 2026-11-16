# Execution Prerequisites

The script requires a Python runtime that provides the standard-library `turtle` and `random` modules.

Normal interactive execution also requires a graphical desktop environment. The program creates a Turtle screen and opens a text-input dialog; a headless terminal without a display cannot provide the intended interaction.

The source defines no package installation step, external service, database, or network dependency. After the race or falsey-input path, `screen.exitonclick()` waits for a user click. See [Runtime Dependencies](RUNTIME_DEPENDENCIES.md) and [Screen Shutdown](SCREEN_SHUTDOWN.md).