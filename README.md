# idfx :zap:

While there is [no support for USB devices on WSL2](https://github.com/microsoft/WSL/issues/4322) for now, this tool comes to help you to flash and monitor [ESP-IDF](https://github.com/espressif/esp-idf) applications on the [WSL2](https://docs.microsoft.com/en-us/windows/wsl/compare-versions).

> **Info:**<br>Tested on [Ubuntu 20.04 LTS](https://www.microsoft.com/en-us/p/ubuntu-2004-lts/9n6svws3rx71) distribution.

# Preview

![idfx preview](preview.gif)

# Usage

```sh
idfx COMMAND PORT [monitor]
```

- `COMMAND`s
    - `flash` - Flash the project.
    - `monitor` - Display serial output.
- `PORT` - Serial COM Port on the Windows. Use Device Manager to find your port.
- `monitor` - This argument can be provided if there is need to flash and monitor with single command (check [examples](#examples)).

# Installation

> **Note:**<br>As a prerequisite for using this tool, [Python :snake:](https://www.python.org) needs to be installed on the Windows.

```sh
# Download idfx

curl -L https://raw.githubusercontent.com/abobija/idfx/main/idfx -o $HOME/.local/bin/idfx && chmod u+x $HOME/.local/bin/idfx

# Now go inside of your project directory, and flash/monitor with next command

idfx flash (PORT) monitor
```

# Examples

| Command  | Description |
| ------------- | ------------- |
| `idfx flash COM2`  | Flashing project using port `COM2` |
| `idfx monitor COM2`  | Display serial output on the port `COM2` |
| `idfx flash COM2 monitor` | Flash project and display serial output, using port `COM2` |

# Author

[abobija](https://github.com/abobija) - [abobija.com](https://abobija.com)

# License

[MIT](LICENSE)