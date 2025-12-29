# Zephyr Logging System Example (Nordic SDK)

This project is a simple application that **demonstrates how the Nordic / Zephyr logging system works**.

The example focuses on **enabling, configuring, and using logs** in a Zephyr-based application.  
It shows how to register a log module and print log messages to the serial console using the Zephyr logging API.

This project was created for learning and testing purposes, aiming to help developers understand **how to properly use the logging infrastructure provided by Zephyr** in Nordic Semiconductor projects.

## Features
- Uses Zephyr logging system
- Demonstrates log module registration
- Prints log messages to the serial console
- Supports different log levels (`LOG_INF`, `LOG_WRN`, `LOG_ERR`, `LOG_DBG`)
- Simple and minimal example focused only on logging

## Logging System
This example demonstrates the basic steps required to use the Zephyr logging system:

- Enable logging support in `prj.conf` using CONFIG_LOG=y
- If memory is constrained, it is possible to use CONFIG_LOG_MODE_MINIMAL=y, hence reducing memory consuming
- Include the logging header in the source code:
  ```c
  #include <zephyr/logging/log.h>
