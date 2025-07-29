| Supported Targets | ESP32 | ESP32-C2 | ESP32-C3 | ESP32-C5 | ESP32-C6 | ESP32-C61 | ESP32-H2 | ESP32-H21 | ESP32-H4 | ESP32-P4 | ESP32-S2 | ESP32-S3 | Linux |
| ----------------- | ----- | -------- | -------- | -------- | -------- | --------- | -------- | --------- | -------- | -------- | -------- | -------- | ----- |

# Hello World Example

Starts a FreeRTOS task to print "Hello World".

(See the README.md file in the upper level 'examples' directory for more information about examples.)

## How to use example

Follow detailed instructions provided specifically for this example.

Select the instructions depending on Espressif chip installed on your development board:

- [ESP32 Getting Started Guide](https://docs.espressif.com/projects/esp-idf/en/stable/get-started/index.html)
- [ESP32-S2 Getting Started Guide](https://docs.espressif.com/projects/esp-idf/en/latest/esp32s2/get-started/index.html)


## Example folder contents

The project **hello_world** contains one source file in C language [hello_world_main.c](main/hello_world_main.c). The file is located in folder [main](main).

ESP-IDF projects are built using CMake. The project build configuration is contained in `CMakeLists.txt` files that provide set of directives and instructions describing the project's source files and targets (executable, library, or both).

Below is short explanation of remaining files in the project folder.

```
├── CMakeLists.txt
├── pytest_hello_world.py      Python script used for automated testing
├── main
│   ├── CMakeLists.txt
│   └── hello_world_main.c
└── README.md                  This is the file you are currently reading
```

For more information on structure and contents of ESP-IDF projects, please refer to Section [Build System](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/api-guides/build-system.html) of the ESP-IDF Programming Guide.

## Troubleshooting

* Program upload failure

    * Hardware connection is not correct: run `idf.py -p PORT monitor`, and reboot your board to see if there are any output logs.
    * The baud rate for downloading is too high: lower your baud rate in the `menuconfig` menu, and try again.

## Technical support and feedback

Please use the following feedback channels:

* For technical queries, go to the [esp32.com](https://esp32.com/) forum
* For a feature request or bug report, create a [GitHub issue](https://github.com/espressif/esp-idf/issues)

We will get back to you as soon as possible.

# ESP32-C5 Hello World Example

A simple demonstration project showing basic functionality of the ESP32-C5 microcontroller using FreeRTOS.

## Project Structure
```
├── CMakeLists.txt            Project build configuration
├── main
│   ├── CMakeLists.txt       Component build configuration
│   └── hello_world_main.c   Main source code
└── README.md                This file
```

## Features
- System information display
- Hardware capability detection
- Memory monitoring
- Auto-restart functionality
- FreeRTOS task demonstration

## Requirements

### Hardware
- ESP32-C5 development board
- USB cable
- Computer running Windows 10/11

### Software
- ESP-IDF v5.5
- Visual Studio Code
- ESP-IDF VS Code Extension
- Python 3.11 or newer

## Getting Started

1. Clone this repository:
```powershell
git clone https://github.com/rajmehta28599/esp32-c5-hello-world.git
cd esp32-c5-hello-world
```

2. Configure the project:
```powershell
idf.py set-target esp32c5
idf.py menuconfig
```

3. Build and flash:
```powershell
idf.py build
idf.py -p COM11 flash monitor
```
Note: Replace `COM11` with your board's actual COM port.

## Sample Output
```
Hello world!
This is esp32c5 chip with 1 CPU core(s), WiFi/BLE, 802.15.4 (Zigbee/Thread)
silicon revision v1.0
2MB embedded flash
Minimum free heap size: 123456 bytes
```

## Troubleshooting
- If flashing fails, verify your COM port number in Device Manager
- For build errors, ensure ESP-IDF is properly installed and configured
- For connectivity issues, check your USB cable connection
- For upload issues, try lowering the baud rate in menuconfig

## Support
- Open an issue on [GitHub](https://github.com/rajmehta28599/esp32-c5-hello-world/issues)
- Visit [esp32.com](https://esp32.com/) forum for technical queries

## License
CC0-1.0

# ESP32-C5 DevKitC-1 Hello World Example

![ESP32-C5 DevKitC-1](https://docs.espressif.com/projects/esp-dev-kits/en/latest/esp32c5/esp32-c5-devkitc-1/_images/esp32-c5-devkitc-1.png)

A demonstration project for the ESP32-C5 DevKitC-1 development board, showcasing basic functionality and system information reporting.

## Board Overview
The ESP32-C5 DevKitC-1 is a cost-effective development board powered by ESP32-C5 series SoCs. Key features include:
- ESP32-C5 RISC-V single-core processor
- 2.4 GHz Wi-Fi 6 (802.11ax)
- Bluetooth 5 (LE)
- IEEE 802.15.4 support
- 400 KB SRAM
- 8 MB flash memory

## Pin Layout
![ESP32-C5 DevKitC-1 Pin Layout](https://docs.espressif.com/projects/esp-dev-kits/en/latest/esp32c5/esp32-c5-devkitc-1/_images/esp32-c5-devkitc-1-pin-layout.png)

## Project Features
- System information display
- Hardware capability detection
- Memory monitoring
- Auto-restart functionality
- FreeRTOS task demonstration

## Requirements

### Hardware
- ESP32-C5 DevKitC-1 board
- USB Type-C cable
- Computer running Windows 10/11

### Software
- ESP-IDF v5.5
- Visual Studio Code
- ESP-IDF VS Code Extension
- Python 3.11 or newer

## Getting Started

1. **Connect the Board**
   - Connect ESP32-C5 DevKitC-1 to your computer using USB Type-C cable
   - Verify the power LED is on
   - Check Device Manager for COM port number

2. **Clone and Configure:**
```powershell
git clone https://github.com/rajmehta28599/esp32-c5-hello-world.git
cd esp32-c5-hello-world
idf.py set-target esp32c5
idf.py menuconfig
```

3. **Build and Flash:**
```powershell
idf.py build
idf.py -p COM11 flash monitor
```
Note: Replace `COM11` with your board's actual COM port.

## Sample Output
```
Hello world!
This is esp32c5 chip with 1 CPU core(s), WiFi/BLE, 802.15.4 (Zigbee/Thread)
silicon revision v1.0
8MB embedded flash
Minimum free heap size: 123456 bytes
```

## Project Structure
```
├── CMakeLists.txt            Project build configuration
├── main
│   ├── CMakeLists.txt       Component build configuration
│   └── hello_world_main.c   Main source code
└── README.md                This file
```

## Hardware Resources
- [ESP32-C5 DevKitC-1 Schematic (PDF)](https://docs.espressif.com/projects/esp-dev-kits/en/latest/esp32c5/esp32-c5-devkitc-1/_static/files/esp32-c5-devkitc-1_v1.0-schematic.pdf)
- [ESP32-C5 Technical Reference Manual](https://docs.espressif.com/projects/esp-idf/en/latest/esp32c5/hw-reference/index.html)

## Troubleshooting
- If flashing fails:
  - Verify COM port number in Device Manager
  - Hold BOOT button while connecting USB cable
  - Try lowering flash frequency in menuconfig
- For connection issues:
  - Check USB Type-C cable connection
  - Verify board power LED is on
  - Try a different USB port

## Support
- [ESP32-C5 Forum](https://esp32.com/)
- [GitHub Issues](https://github.com/rajmehta28599/esp32-c5-hello-world/issues)
- [ESP32-C5 Documentation](https://docs.espressif.com/projects/esp-idf/en/latest/esp32c5/index.html)

## License
CC0-1.0
