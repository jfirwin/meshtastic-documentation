---
layout: page
title: Linux
permalink: /linux
nav_order: 1
parent: Flash Firmware
grand_parent: Getting Started
---
# Linux Firmware Flashing Instructions

Requires `Python` and `pip`

1. Download and unzip the latest Meshtastic firmware [release](https://github.com/meshtastic/Meshtastic-esp32/releases).
2. `pip install --upgrade esptool` - Installs esptool on your machine
3. Connect your radio to your USB port
4. `esptool.py chip_id` - Confirm that your device is talking to your PC by running 
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
5. `cd` into the directory where you unzipped the latest release.
6. Install the correct firmware for your board with `device-install.sh -f firmware-BOARD-VERSION.bin`
   * Example: `./device-install.sh -f firmware-heltec-1.2.x.bin`
7. To update a the firmware on an existing Meshtastic device, run `device-update.sh -f firmware-BOARD-VERSION.bin`
   * Example: `./device-update.sh -f firmware-heltec-1.2.x.bin`
