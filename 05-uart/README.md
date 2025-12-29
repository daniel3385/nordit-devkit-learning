## How it works

when a byte is received and there is inactivity (no new data) after 100 microseconds, or 10 bytes is received, a UART_RX_RDY event is generated.

## Reference

https://docs.nordicsemi.com/bundle/ncs-latest/page/zephyr/hardware/peripherals/uart.html