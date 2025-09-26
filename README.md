Smart Irrigation System Using Arduino Uno –

Overview

This project provides a comprehensive guide to building a Smart Irrigation System that automates watering for plants based on soil moisture levels. It is centered around the use of an Arduino Uno microcontroller, a soil moisture sensor, a relay module, and a DC water pump. This system eliminates manual watering tasks and optimizes water usage, actively promoting healthy plant growth, saving time, and conserving water.

Through real-time monitoring and automated pump control, the Smart Irrigation System ensures that plants are watered only when necessary. The project is beginner-friendly, making it ideal for students, hobbyists, and those interested in integrating IoT (Internet of Things) with agriculture.





Features

Automated Watering: Switches water pump ON/OFF based on real-time soil moisture readings.

Prevents Over-Watering/Under-Watering: Ensures optimal soil moisture for plant health.

Efficient Water Use: Activates pump only when necessary, promoting conservation.

Scalable: Can be expanded for multiple plant beds/zones.

Extension Ready: Add IoT connectivity, displays, or advanced controls.





Components and Requirements
Hardware:


Component	Description

Arduino Uno	Microcontroller, project’s brain
Soil Moisture Sensor	Reads soil moisture and outputs analog signal
DC Water Pump (3–6V)	Waters the plants
Relay Module (5V)	Electrically isolates the high-power pump from Arduino
Jumper Wires	Connects all components
Breadboard/Cables	As required for prototyping/test setup


Software:
Arduino IDE: For writing and uploading code (Download here)

Programming Language: C/C++


Circuit Connections
Connect Soil Moisture Sensor:

VCC → Arduino 5V

GND → Arduino GND

Analog Out → Arduino Analog Pin A0



Connect Relay Module:

VCC → Arduino 5V

GND → Arduino GND

IN → Arduino Digital Pin 7



Wire Pump via Relay:

Pump’s positive wire → Relay NO (Normally Open)

Relay COM → Power supply + terminal

Pump’s negative wire → Power supply – terminal

This configuration allows the relay, controlled by Arduino, to safely switch the pump ON/OFF.


System Workflow


The workflow for the Smart Irrigation System functions as follows:



Start: Power up and initialize the system.

Setup: Arduino configures I/O pins and starts serial communication.

Sensor Reading: Reads the analog value from the soil moisture sensor.

Monitoring: Prints sensor data for calibration and records values each second.




Decision Logic:

If moisture value < threshold (500), it interprets soil as “dry” and activates the pump via relay.

If moisture value ≥ threshold, it detects “wet” and turns the pump OFF.

Delay & Repeat: Waits one second, then repeats the check, creating an automatic loop.

Continuous Loop: The system runs continuously, maintaining ideal soil moisture.

