# Radio-Freqency-Jammer
# WiFi Jammer with nRF24L01

## Overview
This project shows how to create a WiFi jammer using the **nRF24L01** module and an Arduino to disrupt WiFi signals.

## Components
- **Arduino UNO**
- **nRF24L01 Transceiver Module**
- **Jumper Wires**
- **Breadboard**

## Installation
1. Install the **Arduino IDE** from [here](https://www.arduino.cc/en/software).
2. Download the **RF24** library for nRF24L01.

## Wiring
| nRF24L01 Pin | Arduino Pin |
|--------------|-------------|
| GND          | GND         |
| VCC          | 3.3V        |
| CE           | D9          |
| CSN          | D10         |
| SCK          | D13         |
| MOSI         | D11         |
| MISO         | D12         |

## Code
```cpp
#include <SPI.h>
#include <RF24.h>

RF24 radio(9, 10);

void setup() {
  radio.begin();
  radio.setPALevel(RF24_PA_HIGH);
  // Other setup code
}

void loop() {
  // Jammer logic
}
