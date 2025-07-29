# ESP32-C5 DevKitC-1: Hello World Example

This project demonstrates a basic "Hello World" application for the **ESP32-C5 DevKitC-1** development board using FreeRTOS. It showcases essential functionalities, including system information display, hardware capability detection, and memory monitoring.

-----

## Supported Targets

| Supported Targets | ESP32-C5 | ESP32-C51 |
| :---------------- | :------- | :-------- |

-----

## Board Overview

The **ESP32-C5 DevKitC-1** is a cost-effective development board powered by ESP32-C5 series SoCs.

### Key Features

  * **ESP32-C5 RISC-V** single-core processor
  * 2.4 GHz **Wi-Fi 6 (802.11ax)**
  * **Bluetooth 5 (LE)**
  * **IEEE 802.15.4** support (Zigbee/Thread)
  * 400 KB SRAM
  * 8 MB flash memory

-----

## Project Structure

```
├── CMakeLists.txt              Project build configuration
├── main
│   ├── CMakeLists.txt          Component build configuration
│   └── hello_world_main.c      Main source code
└── README.md                   This file
```

-----

## Features

  * System information display
  * Hardware capability detection
  * Memory monitoring
  * Auto-restart functionality
  * FreeRTOS task demonstration

-----

## Requirements

### Hardware

  * **ESP32-C5 DevKitC-1** board
  * USB Type-C cable
  * Computer running Windows 10/11

### Software

  * **ESP-IDF v5.5**
  * **Visual Studio Code**
  * **ESP-IDF VS Code Extension**
  * **Python 3.11** or newer

-----

## Getting Started

Follow these steps to build and flash the "Hello World" example onto your ESP32-C5 DevKitC-1.

1.  **Connect the Board**

      * Connect your ESP32-C5 DevKitC-1 to your computer using a USB Type-C cable.
      * Verify that the power LED on the board is illuminated.
      * Check your Device Manager to identify the **COM port number** assigned to your board.

2.  **Clone and Configure**
    Open your terminal or PowerShell and execute the following commands:

    ```powershell
    git clone https://github.com/rajmehta28599/esp32-c5-hello-world.git
    cd esp32-c5-hello-world
    idf.py set-target esp32c5
    idf.py menuconfig
    ```

3.  **Build and Flash**

    ```powershell
    idf.py build
    idf.py -p COM11 flash monitor
    ```

    **Note:** Replace `COM11` with the actual COM port number of your board.

-----

## Sample Output

Upon successful flashing and monitoring, you should see output similar to this:

```
Hello world!
This is esp32c5 chip with 1 CPU core(s), WiFi/BLE, 802.15.4 (Zigbee/Thread)
silicon revision v1.0
8MB embedded flash
Minimum free heap size: 123456 bytes
```

-----

## Troubleshooting

  * **Program Upload Failure / Flashing Fails**

      * **Hardware connection is not correct:** Run `idf.py -p PORT monitor` and reboot your board to check for output logs.
      * **Incorrect COM port:** Verify the COM port number in Device Manager.
      * **Hold BOOT button:** Hold the BOOT button on the board while connecting the USB cable.
      * **Baud rate too high:** Try lowering your baud rate in the `menuconfig` menu.
      * **Flash frequency:** Try lowering the flash frequency in `menuconfig`.

  * **Build Errors**

      * Ensure **ESP-IDF** is properly installed and configured on your system.
      * Verify that **Python 3.11 or newer** is installed and accessible in your environment path.

  * **Connectivity Issues**

      * Check your **USB cable connection**.
      * Verify the board's **power LED** is on.
      * Try a different **USB port** on your computer.

-----

## Technical Support and Feedback

For further assistance, please use the following channels:

  * **Technical Queries:** Visit the [esp32.com forum](https://esp32.com/).
  * **Feature Requests or Bug Reports:** Create a [GitHub issue](https://github.com/rajmehta28599/esp32-c5-hello-world/issues) in the project repository.
  * **ESP32-C5 Documentation:** Refer to the official [ESP32-C5 documentation](https://docs.espressif.com/projects/esp-idf/en/latest/esp32c5/index.html) for detailed information.

-----

## Hardware Resources

  * [ESP32-C5 DevKitC-1 Schematic (PDF)](https://docs.espressif.com/projects/esp-dev-kits/en/latest/esp32c5/esp32-c5-devkitc-1/_static/files/esp32-c5-devkitc-1_v1.0-schematic.pdf)
  * [ESP32-C5 Technical Reference Manual](https://docs.espressif.com/projects/esp-idf/en/latest/esp32c5/hw-reference/index.html)

-----

## License

CC0-1.0