# idfx :zap:

While there is [no support for USB devices on WSL2](https://github.com/microsoft/WSL/issues/4322) for now, this tool comes to help you to flash and monitor [ESP-IDF](https://github.com/espressif/esp-idf) and [ESP8266_SDK](https://github.com/espressif/ESP8266_RTOS_SDK) applications on the [WSL2](https://docs.microsoft.com/en-us/windows/wsl/compare-versions).

> **Info:**<br>Tested on [Ubuntu 20.04 LTS](https://www.microsoft.com/en-us/p/ubuntu-2004-lts/9n6svws3rx71) and [Debian](https://www.microsoft.com/en-us/p/debian/9msvkqc78pk6) distributions.

> **Note:**<br>As a prerequisite for using this tool, [Python :snake:](https://www.python.org) needs to be installed on the Windows.

# Usage

```sh
idfx COMMAND [PORT]
```

- `COMMAND`s
    - `build`       - Build the project (alias for `idf.py build`).
    - `flash`       - Flash the project.
    - `monitor`     - Display serial output.
    - `all`         - Build project, flash and monitor serial output.
    - `erase_flash` - Erase the entire flash content.
  	-  `set-target` - Set target (alias for idf.py set-target [TARGET])
	-  `menuconfig` - Configure (alias for idf.py menuconfig)
- `PORT` - Serial COM Port on the Windows. Use Device Manager to find your port.

# Installation

Execute next command inside of your WSL to install `idfx`

```sh
wget https://raw.githubusercontent.com/abobija/idfx/main/idfx -O $HOME/.local/bin/idfx && chmod u+x $HOME/.local/bin/idfx
```

# Supported ESP-IDF versions

idfx supports:
- [ESP-IDF](https://github.com/espressif/esp-idf) version 4.0 and above
- [ESP8266_SDK](https://github.com/espressif/ESP8266_RTOS_SDK) version 3.0 and above

# Examples

| Command  | Description |
| ------------- | ------------- |
| `idfx build`  | Building project (alias for `idf.py build`) |
| `idfx flash COM2`  | Flashing project using port `COM2` |
| `idfx monitor COM2`  | Display serial output on the port `COM2` |
| `idfx all COM2` | Build project, flash and monitor serial output, using port `COM2` |
| `idfx flash COM2 monitor` | Flash project and display serial output, using port `COM2` |
| `idfx erase_flash COM2` | Erase the entire flash, using port `COM2` |

# [How to install ESP-IDF on WSL2 and build/flash/monitor?](https://gist.github.com/abobija/2f11d1b2c7cb079bec4df6e2348d969f)

# Preview

![idfx preview](preview.gif)

# Author

[abobija](https://github.com/abobija) - [abobija.com](https://abobija.com)

# License

[MIT](LICENSE)
