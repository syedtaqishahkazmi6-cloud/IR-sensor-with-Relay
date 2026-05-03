# IR Sensor Controlled Relay System

This project uses an Arduino Nano to trigger a single-channel relay based on input from an Infrared (IR) proximity sensor.

## Component List
* Arduino Nano
* IR Obstacle Avoidance Sensor (3-pin)
* 5V Single-Channel Relay Module
* Jumper Wires

## Pinout Configuration

| Component | Pin Label | Arduino Nano Pin |
| :--- | :--- | :--- |
| **IR Sensor** | VCC | 5V |
| | GND | GND |
| | OUT | D2 |
| **Relay Module** | VCC / + | 5V |
| | GND / - | GND |
| | IN | D3 |

## Logic Overview
* **IR Sensor:** Most standard IR modules use "Active LOW" logic. This means the `OUT` pin stays `HIGH` normally and pulses `LOW` when an object is detected.
* **Relay Module:** Most 5V relay modules are "Active LOW," meaning the relay engages when the `IN` pin is pulled to `GND` (LOW).

## Wiring Diagram Reference


## Usage Instructions
1. Connect the components according to the pinout table.
2. Power the Arduino via USB.
3. Adjust the small potentiometer on the IR sensor to change the detection sensitivity/distance.
4. When the IR sensor's onboard LED lights up (detection), the relay should click and activate the connected load.