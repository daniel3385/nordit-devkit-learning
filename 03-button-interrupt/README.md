# Button and LED Example (Switch 0) using interrupt

This project is a simple application that **reads the button Switch 0 using GPIO interruption** and **toggles the LED when the button is pressed**.

The button is configured as a GPIO input with an **interrupt handler**, allowing the system to detect button presses efficiently without continuous polling.  
When Switch 0 is pressed, an interrupt is triggered and the LED turns on. When the button is released, the LED turns off.

This project was created for learning and testing purposes.

## Features
- Button input using GPIO interrupt
- Controls LED using GPIO interrupt callback
- LED toggles when button is pressed
- Printf message to the serial using printk when button pressed

## Hardware
- Nordic Semiconductor development board
- Switch 0
- On-board LED
