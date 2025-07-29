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

# ESP32-C5 Hello World Demo

A demonstration project for the ESP32-C5 microcontroller that showcases basic functionality and system information reporting.

## Features
- System information display
- WiFi/BLE/802.15.4 capability detection
- Flash memory size reporting
- Heap memory monitoring
- Automatic system restart demonstration

## Prerequisites
- ESP-IDF v5.5
- Visual Studio Code with ESP-IDF extension
- ESP32-C5 development board
- Windows 10/11 with Python 3.11+

## Quick Start

1. Clone the repository:
```bash
git clone https://github.com/rajmehta28599/esp32-c5-hello-world.git
cd esp32-c5-hello-world
```

2. Set the correct target:
```bash
idf.py set-target esp32c5
```

3. Build the project:
```bash
idf.py build
```

4. Flash and monitor (replace COM11 with your port):
```bash
idf.py -p COM11 flash monitor
```

## Output Example
```
Hello world!
This is esp32c5 chip with 1 CPU core(s), WiFi/BLE, 802.15.4 (Zigbee/Thread)
silicon revision v1.0
2MB embedded flash
Minimum free heap size: 123456 bytes
```

## License
This project is licensed under CC0-1.0

## Contributing
Feel free to open issues or submit pull requests for improvements.
