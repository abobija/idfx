# idfx :zap:

While there is [no support for USB devices on WSL2](https://github.com/microsoft/WSL/issues/4322) for now, this tool comes to help you to flash and monitor your [ESP-IDF](https://github.com/espressif/esp-idf) applications on the [WSL2](https://docs.microsoft.com/en-us/windows/wsl/compare-versions).

> **Info:**<br>Tested on [Ubuntu 20.04 LTS](https://www.microsoft.com/en-us/p/ubuntu-2004-lts/9n6svws3rx71) distribution.

# Preview

![idfx preview](preview.gif)

# Usage

```sh
idfx COMMAND PORT
```

- `COMMAND`s
    - `flash` - Flash the project.
    - `monitor` - Display serial output.
- `PORT` - Serial COM Port on the Windows. Use Device Manager to find your port.

# Installation

> **Note:**<br>As a prerequisite for using this tool, [Python :snake:](https://www.python.org) needs to be installed on the Windows.

```sh
# Create ~/bin directory (if it doesn't exist) and cd into it

mkdir -p ~/bin && cd ~/bin

# Download idfx into ~/bin

curl -L -o idfx https://raw.githubusercontent.com/abobija/idfx/main/idfx

# Mark idfx as executable

chmod u+x idfx

# Add ~/bin to PATH by sourcing ~/.profile script (inside of profile script there is command that adds ~/bin to PATH only if that dir exists)

. ~/.profile

# Now you can go inside of your project directory, build project, and then execute

# idfx flash (PORT)
# idfx monitor (PORT)
```

# Examples

| Command  | Description |
| ------------- | ------------- |
| `idfx flash COM2`  | Flashing project using port `COM2` |
| `idfx monitor COM2`  | Display serial output on the port `COM2` |

# Author

[abobija](https://github.com/abobija) - [abobija.com](https://abobija.com)

# License

[MIT](LICENSE)