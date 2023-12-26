# Overview

This repository contains a configuration file that can be used to flash a [Tuya DY-RQ400A Combustible Gas Alarm](https://expo.tuya.com/product/602455) with ESPHome using Libretiny as it has a [WB2S](https://docs.libretiny.eu/boards/wb2s/) (BK7231T) chip built-in.

# Flashing

Flashing can be done via [UART1](https://docs.libretiny.eu/boards/wb2s/#pinout) using an UART. The chip requires 3.3V to be powered on:

```bash
python3 -m venv esphome-venv
. esphome-venv/bin/activate
pip3 install esphome
esphome run --device /dev/<your-serial-device-name> <path-to>/gas-alarm-DY-RQ400A.yaml
```

# OTA

Make sure the device has a stable Wi-Fi connection, otherwise attaching to UART again will be needed again if OTA is interrupted.

```bash
python3 -m venv esphome-venv
. esphome-venv/bin/activate
pip3 install esphome
esphome run --device <device-ip> <path-to>/gas-alarm-DY-RQ400A.yaml
```
