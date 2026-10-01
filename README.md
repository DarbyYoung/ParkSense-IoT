# ParkSense - IoT Smart Parking System

ParkSense is an IoT-based smart parking system developed using an ESP32. The system monitors two parking bays and controls vehicle entry based on the number of available parking spaces.

## Features

- Two parking bay ultrasonic sensors
- Entrance ultrasonic sensor
- Automatic parking space detection
- AVAILABLE, POSSIBLE VEHICLE and OCCUPIED detection states
- LED indicators for parking bay availability
- Servo-controlled entrance barrier
- Buzzer warning when the parking area is full
- MQTT communication using HiveMQ Cloud
- Real-time monitoring using Node-RED
- Historical data storage and visualisation using ThingSpeak
- Rule-based edge intelligence using consecutive sensor readings
- MQTT authentication and secure communication

## Hardware

- ESP32
- 3 × HC-SR04 Ultrasonic Sensors
- 4 × LEDs
- Servo Motor
- Buzzer
- Resistors

## IoT Architecture

ParkSense uses a layered IoT architecture:

1. Perception Layer - Ultrasonic sensors detect vehicles.
2. Processing Layer - ESP32 processes sensor readings and performs automation.
3. Network Layer - Wi-Fi, MQTT and HTTPS are used for communication.
4. Application Layer - Node-RED provides real-time monitoring and ThingSpeak provides historical data visualisation.

## Edge Intelligence

The system uses consecutive ultrasonic sensor readings to reduce false occupancy detections.

Each parking bay can have one of three states:

- AVAILABLE
- POSSIBLE VEHICLE
- OCCUPIED

A parking bay is only confirmed as occupied after three consecutive vehicle detections.

## Project Files

- `sketch.ino` - ESP32 source code
- `diagram.json` - Wokwi circuit configuration
- `libraries.txt` - Required Wokwi libraries

## Security

Passwords and API keys have been removed from the public source code. Users must provide their own HiveMQ and ThingSpeak credentials before running the project.

## Author

Darby Young & Nicholas Smith 

3707ICT - Automation and IoT
