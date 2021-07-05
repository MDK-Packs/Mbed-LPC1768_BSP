# Mbed LPC1768

## Overview

The Mbed NXP LPC1768 development board is designed for prototyping all sorts of devices, especially those including Ethernet, USB, and the flexibility of lots of peripheral interfaces and flash memory. It is packaged as a small DIP form-factor for prototyping with through-hole PCBs, stripboard and breadboard, and includes a built-in CMSIS-DAP debug adapter.

It is based on the NXP LPC1768, with a 32-bit Arm Cortex-M3 core running at 96 MHz. It includes 512 KB flash memory, 32 KB RAM and lots of interfaces including built-in Ethernet, USB Host and Device, CAN, SPI, I2C, ADC, DAC, PWM and other I/O interfaces. The pinout below shows the commonly used interfaces and their locations. Note that all the numbered pins (P5 - P30) can also be used as digital input and output interfaces.

## Pinout

![Mbed LPC1768 Pin-Out](./lpc1768_pinout.png "Mbed LPC1768 Pin-Out")

| Pin | Function     | Alternate Function |
|-----|--------------|--------------------|
| GND | Ground       |                    |
| VIN | 4.5 V - 9 V  |                    |
| VB  | VBat         |                    |
| nR  | nRESET       |                    |
| P5  | SPI MOSI     |                    |
| P6  | SPI MISO     |                    |
| P7  | SPI SCK      |                    |
| P8  | Digital I/O  |                    |
| P9  | UART TX      | I2C SDA            |
| P10 | UART RX      | I2C SCL            |
| P11 | SPI MOSI     |                    |
| P12 | SPI MISO     |                    |
| P13 | SPI SCK      | UART TX            |
| P14 | UART RX      |                    |
| P15 | AnalogIn     |                    |
| P16 | AnalogIn     |                    |
| P17 | AnalogIn     |                    |
| P18 | AnalogIn     | AnalogOut          |
| P19 | AnalogIn     |                    |
| P20 | AnalogIn     |                    |
| P21 | PWMOut       |                    |
| P22 | PWMOut       |                    |
| P23 | PWMOut       |                    |
| P24 | PWMOut       |                    |
| P25 | PWMOut       |                    |
| P26 | PWMOut       |                    |
| P27 | UART RX      | I2C SCL            |
| P28 | UART TX      | I2C SDA            |
| P29 | CAN TD       |                    |
| P30 | CAN RD       |                    |
| D+  | USB D+       |                    |
| D-  | USB D-       |                    |
| TD+ | Ethernet TD+ |                    |
| TD- | Ethernet TD- |                    |
| RD+ | Ethernet RD+ |                    |
| RD- | Ethernet RD- |                    |
| IF+ |              |                    |
| IF- |              |                    |
| VU  | 5 V USB Out  |                    |
| VOUT| 3.3 V Out    |                    |

## Schematics

- [Mbed LPC1768 development board schematic](./mbed-005.1.pdf)

## CMSIS-Drivers

This board support pack contains a CMSIS-Driver for the [VIO](https://arm-software.github.io/CMSIS_5/develop/Driver/html/group__vio__interface__gr.html) interface. This is a virtual I/O abstraction for peripherals that are typically used in example projects. The **Blinky** example uses this interface to create a running light with the four LEDs mounted on the board.

## Firmware

Make sure that you have updated your CMSIS-DAP firmware to the latest version. This makes the board compatible with [Keil Studio Cloud](https://keil.arm.com) that enables browser-based project creation and debugging:

- [CMSIS-DAP firmware](./mbed_if.axf.if)