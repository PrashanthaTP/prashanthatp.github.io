---
title: Bit Of Everything
date: 2026-05-10 +0530
categories: [PROGRAMMING, GENERAL]
tags: [c,cpp,python,protocols]     # TAG names should always be lowercase
---
# Protocols

## UART

- Asynchronous, Half Duplex Serial Communication
- Used for logging, bluetooth, WIFI, LCD
## SPI

- Serial Peripheral Interface
- Synchronous, Full Duplex
- Connecting microcontroller and sensors
- Faster than UART and I2C
- Four wires
  + SCLK  : Clock
  + MISO  : Master In Slave Out
  + MOSI  : Master Out Slave In
  + CS/SS : Chip/Slave select
- EEPROMS, Display, low latency

## I2C

- Two wire, serial communication
- SDL, SCL
- Half Duplex
- ADC, DAC, non volatile memory


# Memory in Microcontrollers

## Flash Memory
- For storing code

## RAM
- SRAM/DRAM
- SRAM: Cache
- DRAM: Device RAM
- Stack, Program local variables

## EEPROM
- Configuration/Calibration data


# Python

## Logging

```python
import logging

logging.basicConfig(filename="main.log", level=logging.INFO)
logger = logging.getLogger(__name__)
logger.info("Hello World!!")
```

## JSON

```python
import json
data = {}
with open("input.json", 'r') as file:
    data = json.load(file)

with open("output.json", 'w') as file:
    json.dump(data, file)
```

