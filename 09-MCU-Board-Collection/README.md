# MCU & IoT Board Collection

Smaller boards built while developing layout fundamentals — grouped here rather
than given individual repos.

| Board | MCU | Layers | Notable |
|---|---|---|---|
| General-purpose IoT board | ESP32-WROOM | 4 | Si7021 temp/humidity · CP2104 USB-UART · QWIIC · RGB LED · power relay · fused supply |
| IoT control board | ESP32-C3 WROOM | — | 12V→5V→3.3V rails · 5A handling · T90 relay · onboard fuse · separate USB-UART programming board |
| IoT dev board | ESP32-S3 (8MB) | 4 | USB-C power + programming · Si7021 · QWIIC + SPI headers · BOOT/RESET · RGB LED |
| MSPM0 board | TI MSPM0 (Cortex-M0+) | — | First TI ARM design — decoupling, crystal layout, USB diff pairs per datasheet |
| STM32 "Black Pill" | STM32 | 2 | First full 2-layer design — 3.3V LDO, reset circuit, BOOT config, USB micro |
| DeskBuddy v2 | ESP32-C3 | — | IP5306 (charge + protect + 5V boost in one IC), TTP223 touch pad etched onto board, OLED with live battery indicator |
| Analog automation controller | None | — | 3× NE555 + BC547 conductivity sensing, 5 relays, 30-min interval logic — zero firmware |

## Notes
The ESP32/STM32 boards share a lot of DNA by design — each one was a deliberate
repetition to build layout speed and consistency. The MSPM0 and analog controller
are the outliers worth a look.
