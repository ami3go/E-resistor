# E-Resistor

E-Resistor is a programmable resistor matrix board (RP2040 + W5500) controlled over Ethernet via SCPI. This repository is a landing page / index for the project — the actual code lives in the repositories below.

## Repositories

| Repo | Description |
|---|---|
| [E-resistor-matrix-firmware](https://github.com/ami3go/E-resistor-matrix-firmware) | RP2040 dual-core firmware for the resistor matrix board |
| [E-resistor-matrix-python-driver](https://github.com/ami3go/E-resistor-matrix-python-driver) | Python driver (`eresistor_driver`) for SCPI-over-TCP / HTTP control from a PC |
| [E-resistor-matrix-calibration-tool](https://github.com/ami3go/E-resistor-matrix-calibration-tool) | Calibration GUI tool for the resistor matrix (private) |
| [E-resistor-relay-8bits](https://github.com/ami3go/E-resistor-relay-8bits) | 8-bit relay-based resistor switch board |

## Overview

- The board exposes SCPI control on TCP port `5025` and helper HTTP endpoints (`/ping`, `/identify_led`, calibration-file download) on port `80`.
- **python-driver** provides a high-level client (`EResistorClient`) for channel control, calibration download, equivalent-resistance calculation, closest-mask solving, and more. See its README for usage examples.
- **firmware** contains the embedded RP2040 firmware, including stable releases and bring-up/regression test material.
- **calibration-tool** provides a GUI for generating/managing the calibration data consumed by the driver and firmware.
- **relay-8bits** provides a transport-agnostic Python driver (`eresistor_relay8bits`) for the 8-relay resistor board, supporting up to 128 channels with per-(IP, channel) calibration; see its README for examples and setup.

Each repository has its own README, issues, and history — follow the links above for details.
