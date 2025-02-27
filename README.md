# Blood Oxygen & Heart Rate Monitor with MAX30100 Pulse Oximeter & Arduino

## Introduction
In this project, we will create a device that can measure Blood Oxygen (SpO2) & Heart Rate (BPM) using the MAX30100 Pulse Oximeter and Arduino. The blood oxygen concentration (SpO2) is measured in percentage, and the heart rate is measured in BPM. We can also use the MAX30102, which is an upgraded version of the MAX30100.

The measured SpO2 and BPM values will be displayed on a 0.96″ OLED Display. With each heartbeat, the display value updates on the OLED screen. Additionally, by using a Bluetooth module (HC-05/HC-06) in slave mode, we can wirelessly send data to an Android app, enabling real-time monitoring and data logging. This wearable device can be particularly useful for athletes to track their heart rate and oxygen levels during workouts.

## How Does a Pulse Oximeter Work?
Oxygen enters the lungs and is absorbed into the bloodstream, where it binds to hemoglobin and is transported to various organs. A pulse oximeter measures oxygen saturation by using light absorption in oxygenated and deoxygenated blood.

A small clamp-like device is placed on a finger, earlobe, or toe. It emits small beams of light through the blood, measuring the amount of oxygen by detecting changes in light absorption.

## MAX30100 Pulse Oximeter
The MAX30100 sensor is an integrated pulse oximetry and heart rate monitor solution. It includes:
- Two LEDs (red and infrared)
- A photodetector
- Optimized optics
- Low-noise analog signal processing

It operates from 1.8V and 3.3V power supplies and can be powered down via software with negligible standby current.

### Features:
- Low power consumption (1.8V and 3.3V operation)
- Ultra-low shutdown current (0.7µA typical)
- Fast data output capability

## Working of MAX30100 Pulse Oximeter and Heart-Rate Sensor
The device uses two LEDs:
- **Infrared Light** (for pulse rate measurement)
- **Red & Infrared Light** (for oxygen level measurement)

When the heart pumps blood, the volume of oxygenated blood increases, leading to changes in light absorption. The MAX30100 sensor detects these changes and stores the data, which is then retrieved via I2C communication.

- **Oxygenated Blood** absorbs more infrared light and allows more red light to pass.
- **Deoxygenated Blood** absorbs more red light and allows more infrared light to pass.

By analyzing these absorption levels, the sensor determines the pulse rate and oxygen saturation levels.

## Circuit Diagram & Connections
The circuit diagram for interfacing the MAX30100 Pulse Oximeter with Arduino, along with the HC-05 Bluetooth Module & OLED Display, is shown below.

### Connections:
- **MAX30100 & OLED Display** use I2C communication:
  - SDA → A4 (Arduino)
  - SCL → A5 (Arduino)
- **HC-05 Bluetooth Module** uses UART communication:
  - TX → RX (Arduino)
  - RX → TX (Arduino)

## Required Components
- **Arduino Board** (Uno/Nano)
- **MAX30100 Pulse Oximeter**
- **0.96” OLED Display**
- **HC-05/HC-06 Bluetooth Module**
- **Jumper Wires**
- **Power Supply (5V)**

## Usage
1. Connect all components as per the circuit diagram.
2. Upload the Arduino code to read data from the MAX30100 sensor.
3. Monitor the SpO2 and BPM values on the OLED display.
4. Use a Bluetooth module to transmit the data to an Android app for remote monitoring.

## Applications
- Health Monitoring
- Fitness Tracking for Athletes
- Remote Patient Monitoring

## License
This project is open-source and available under the MIT License.

---
Feel free to contribute to this project by submitting pull requests or reporting issues!
