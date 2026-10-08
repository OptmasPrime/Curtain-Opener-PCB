# For the ESP32 C3 Supermini




| ESP32-C3 Pin | Default Use | Your PCB Custom Assignment |
| :--- | :--- | :--- |
| GPIO 0 | General I/O | TMC2209 STEP Pulse |
| GPIO 1 | General I/O | TMC2209 DIR Direction |
| GPIO 2 | Strapping Pin | Battery Voltage Monitor (ADC1_CH2) |
| GPIO 3 | General I/O | TMC2209 DIAG (Homing Only) |
| GPIO 4 | I2C SDA | Sensor I2C SDA |
| GPIO 5 | General I/O | Sensor I2C SCL |
| GPIO 6 | I2C SCL | TMC2209 Single-Wire UART |
| GPIO 7 | SPI MOSI | |
| GPIO 8 | Onboard LED | |
| GPIO 9 | BOOT Button | |
| GPIO 10 | SPI CS | Physical Toggle Button (Wake Capable) |
| GPIO 20 | UART RX |  |
| GPIO 21 | UART TX | Motor EN Pin |

GPIO 20 used to have the **_USB Charge Isolation Circuit_**, but removed it