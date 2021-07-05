Blinky project
==============

The **Blinky** project is a simple example that can be used to verify the
basic tool setup.

It is compliant to the Cortex Microcontroller Software Interface Standard (CMSIS)
and uses the CMSIS-RTOS2 API interface for RTOS functionality. The CMSIS-RTOS2 API
is available with various real-time operating systems, for example RTX5 or FreeRTOS.

Operation
---------

The application shows a running light on all four LEDs with an interval of 1 second.

The board hardware mapping of vioLED0 depends on the configuration of the
CMSIS-Driver VIO.
