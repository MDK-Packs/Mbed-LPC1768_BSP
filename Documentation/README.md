# Mbed LPC1768

## Overview

The Mbed NXP LPC1768 development board is designed for prototyping all sorts of devices, especially those including Ethernet, USB, and the flexibility of lots of peripheral interfaces and flash memory. It is packaged as a small DIP form-factor for prototyping with through-hole PCBs, stripboard and breadboard, and includes a built-in CMSIS-DAP debug adapter.

It is based on the NXP LPC1768, with a 32-bit Arm Cortex-M3 core running at 96 MHz. It includes 512 KB flash memory, 32 KB RAM and lots of interfaces including built-in Ethernet, USB Host and Device, CAN, SPI, I2C, ADC, DAC, PWM and other I/O interfaces. The pinout below shows the commonly used interfaces and their locations. Note that all the numbered pins (P5 - P30) can also be used as digital input and output interfaces.

## Pinout

![Mbed LPC1768 Pin-Out](./lpc1768_pinout.png "Mbed LPC1768 Pin-Out")

| Pin | Function     | Alternate Function |
|-----|--------------|--------------------|
| GND | Ground       | N/A                |
| VIN | 4.5 V - 9 V  | N/A                |
| VB  | VBat         | N/A                |
| nR  | nRESET       | N/A                |
| P5  | SPI MOSI     | N/A                |
| P6  | SPI MISO     | N/A                |
| P7  | SPI SCK      | N/A                |
| P8  | N/A          | N/A                |
| P9  | UART TX      | I2C SDA            |
| P10 | UART RX      | I2C SCL            |
| P11 | SPI MOSI     | N/A                |
| P12 | SPI MISO     | N/A                |
| P13 | SPI SCK      | UART TX            |
| P14 | UART RX      | N/A                |
| P15 | AnalogIn     | N/A                |
| P16 | AnalogIn     | N/A                |
| P17 | AnalogIn     | N/A                |
| P18 | AnalogIn     | AnalogOut          |
| P19 | AnalogIn     | N/A                |
| P20 | AnalogIn     | N/A                |
| P21 | PWMOut       | N/A                |
| P22 | PWMOut       | N/A                |
| P23 | PWMOut       | N/A                |
| P24 | PWMOut       | N/A                |
| P25 | PWMOut       | N/A                |
| P26 | PWMOut       | N/A                |
| P27 | UART RX      | I2C SCL            |
| P28 | UART TX      | I2C SDA            |
| P29 | CAN TD       | N/A                |
| P30 | CAN RD       | N/A                |
| D+  | USB D+       | N/A                |
| D-  | USB D-       | N/A                |
| TD+ | Ethernet TD+ | N/A                |
| TD- | Ethernet TD- | N/A                |
| RD+ | Ethernet RD+ | N/A                |
| RD- | Ethernet RD- | N/A                |
| IF+ |              | N/A                |
| IF- |              | N/A                |
| VU  | 5 V USB Out  | N/A                |
| VOUT| 3.3 V Out    | N/A                |

## Schematics

- [Mbed LPC1768 development board schematic](./mbed-005.1.pdf)

## CMSIS-Drivers

This board support pack contains a CMSIS-Driver for the [VIO](https://arm-software.github.io/CMSIS_5/develop/Driver/html/group__vio__interface__gr.html) interface. This is a virtual I/O abstraction for peripherals that are typically used in example projects. The **Blinky** example uses this interface to create a running light with the four LEDs mounted on the board.

## Firmware

Make sure that you have updated your CMSIS-DAP firmware to the latest version. This makes the board compatible with [Keil Studio Cloud](https://keil.arm.com) that enables browser-based project creation and debugging:

- [CMSIS-DAP firmware](./mbed_if.axf.if)