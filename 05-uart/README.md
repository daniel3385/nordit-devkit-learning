# UART LED Control Example

This project demonstrates the use of **UART serial communication** in the nRF Connect SDK to control LEDs on a development board.

## What the code does

- Initializes the UART peripheral using the asynchronous API.
- Configures multiple LEDs as GPIO outputs.
- Continuously listens for incoming data on the UART interface.
- When a character is received:
  - Sending `'1'` toggles LED 1
  - Sending `'2'` toggles LED 2
  - Sending `'3'` toggles LED 3
- UART reception is automatically re-enabled to allow continuous command input.

## Usage

Send characters (`1`, `2`, or `3`) through a serial terminal connected to the board’s UART interface to toggle the corresponding LEDs.

## Reference

https://docs.nordicsemi.com/bundle/ncs-latest/page/zephyr/hardware/peripherals/uart.html