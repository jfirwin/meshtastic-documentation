---
layout: page
title: MacOS
permalink: /mac-os
nav_order: 1
parent: Flash Firmware
grand_parent: Getting Started
---
# MacOS Firmware Flashing Instructions

1. Download and unzip the latest Meshtastic firmware [release](https://github.com/meshtastic/Meshtastic-esp32/releases).
2. Download [ESPHome Flasher](https://github.com/esphome/esphome-flasher/releases).
3. Connect your radio to your USB port and open ESPHome Flasher.
4. If your board is not showing under Serial Port then you likely need to install the drivers for the CP210X serial chip. In Windows you can check by searching “Device Manager” and ensuring the device is shown under “Ports”.
5. If there is an error, download the [drivers](https://www.silabs.com/products/development-tools/software/usb-to-uart-bridge-vcp-drivers), then unzip and run the Installer application.
6. In ESPHome Flasher, refresh the serial ports and select the port to which your board is connected.
7. Browse to the previously downloaded firmware and select the correct firmware based on the board type.
8. Select Flash ESP.
9. Once complete, “Done! Flashing is complete!” will be shown.
10. The board will boot and show the Meshtastic logo.
11. Debug messages sent from the Meshtastic device can be viewed with a terminal program such as PuTTY. Within PuTTY, click “Serial”, enter the “Serial line” com port (can be found at step 4), enter “Speed” as 921600, then click “Open”.

Firmware Flashing from Commandline

Installing on OS X through the commandline uses the same method as linux, but requires a slightly different method to install Python, pip and esptool.

OS X (10.15.3/Catalina) comes with Python 2.7 installed, but not pip.

1. `brew install pyenv` - Installs PyEnv
2. `pyenv install 3.7.7` - To install and select Python 3.7.7
3. `pyenv global 3.7.7` - Selects the new version of Python
4. `brew install pip` - Installs pip3
5. `pip3 install --upgrade esptool` - Installs esptool

You may need to install a driver from Silicon Labs for the [CP210X USB to UART bridge](https://www.silabs.com/products/development-tools/software/usb-to-uart-bridge-vcp-drivers)

6. Download and unzip the latest Meshtastic firmware [release](https://github.com/meshtastic/Meshtastic-esp32/releases).
7. `pip install --upgrade esptool` - Installs esptool on your machine
8. Connect your radio to your USB port
9. `esptool.py chip_id` - Confirm that your device is talking to your PC by running 
You should see something like:
```
mydir$ esptool.py chip_id
esptool.py v2.6
Found 2 serial ports
Serial port /dev/ttyUSB0
Connecting....
Detecting chip type... ESP32
Chip is ESP32D0WDQ6 (revision 1)
Features: WiFi, BT, Dual Core, 240MHz, VRef calibration in efuse, Coding Scheme None
MAC: 24:6f:28:b5:36:71
Uploading stub...
Running stub...
Stub running...
Warning: ESP32 has no Chip ID. Reading MAC instead.
MAC: 24:6f:28:b5:36:71
Hard resetting via RTS pin...
```
10. `cd` into the directory where you unzipped the latest release.
11. Install the correct firmware for your board with `device-install.sh -f firmware-BOARD-VERSION.bin`
   * Example: `./device-install.sh -f firmware-heltec-1.2.x.bin`
12. To update a the firmware on an existing Meshtastic device, run `device-update.sh -f firmware-BOARD-VERSION.bin`
   * Example: `./device-update.sh -f firmware-heltec-1.2.x.bin`
13. The board will boot and show the Meshtastic logo.