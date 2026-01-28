# Automated Self-Watering Plant System

This project is an **automated self-watering system** built using an Arduino-compatible microcontroller. It monitors environmental conditions such as soil moisture, light level, temperature, humidity, and water tank level, and automatically dispenses water when needed.

The system provides real-time feedback through an LCD display and includes fail-safe mechanisms to prevent operation when the water tank is empty.

## Project Overview
The goal of this project is to reduce manual plant care by automating watering decisions based on sensor data. A menu-driven LCD interface allows users to view live sensor readings, while a relay-controlled pump and servo motor manage water dispensing and tank status.

> **Note:** This repository contains only my embedded software contribution. The physical enclosure (flower pot) was designed separately by another team member.

## Features
- Automatic watering based on soil moisture level  
- Real-time temperature and humidity monitoring  
- Light level detection using an LDR  
- Water tank level monitoring using an ultrasonic sensor  
- LCD menu system controlled by a push button  
- Servo-controlled trap door for low water warnings  
- Relay-controlled water pump  

## How the System Works
- A **soil moisture sensor** checks if the soil is below a defined threshold  
- If moisture is too low, the **relay activates the water pump**  
- An **ultrasonic sensor** measures the distance to determine the water tank level  
- If the tank is nearly empty, a **servo opens a trap door** as a visual alert  
- A **16x2 I2C LCD** displays:
  - Temperature & humidity
  - Light level
  - Soil moisture level
  - Water tank level  
- A **push button** cycles through the LCD menu options  

## Sensor Threshold Logic
- Water is dispensed when soil moisture drops below a predefined threshold  
- The system prevents normal operation when the water tank level is too low  
- Servo position is adjusted based on remaining water level  

## My Contribution
- Designed and implemented the **entire embedded control system**
- Integrated and programmed all sensors and actuators
- Developed the LCD menu interface and button navigation
- Implemented automatic watering logic and fail-safe mechanisms

## Other Team Contributions
- **CAD Design:** Another team member designed the **3D CAD flower pot enclosure**, ensuring proper placement and housing of all hardware components.

## Hardware Components
- Arduino-compatible microcontroller  
- Soil moisture sensor (analog & digital)  
- DHT11 temperature & humidity sensor  
- LDR (light-dependent resistor)  
- Ultrasonic distance sensor  
- Servo motor  
- Relay module  
- 16x2 I2C LCD  
- Push button  

## Libraries Used
- `Wire.h`
- `LiquidCrystal_I2C.h`
- `DHT.h`
- `NewPing.h`
- `Servo.h`

## Programming Language
- **C / C++ (Arduino)**

## Notes
This repository represents my complete software contribution to the project. Hardware wiring and CAD design are not included.
