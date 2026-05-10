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
## Exception Handling

```python
def main():
    try:
        a = input("a: ")
        b = input("b: ")
        c = a//b
        print(c)
    except Exception as e:
        print(e)
    else:
        print("else")
    finally:
        print("finally")

if __name__ == "__main__":
    main()

"""
Example 1:

a: 1
b: 0
Exception occured.
integer division or modulo by zero
finally


Example 2:

a: 1
b: 1
a//b:  1
else
finally

"""
```

# OS

## Process vs Threads

**Process** is an independent executing program with its own memory space,
whereas a **thread** is a smaller execution unit within a process which shares
resources with other threads in the same process.

![process_vs_threads_memory_space](/assets/images/programming/Process_vs_Threads_1.png)

- Threads are faster to create and context switch (less overhead) compared to processes.
- Inter Thread Communication is easier compared to Inter Process Communication.
- If one process crashes, other processes generally continue to run, whereas if a thread crashes,
the parent process can crash too.
