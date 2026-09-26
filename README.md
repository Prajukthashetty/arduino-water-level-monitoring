Object Distance Monitoring System 📏

Overview

This project is an Object Distance Monitoring System built using an Arduino UNO and an HC-SR04 ultrasonic sensor.

The system measures the distance between the sensor and an object and uses three LEDs and a buzzer to indicate different distance levels.

Components Used

- Arduino UNO
- HC-SR04 Ultrasonic Sensor
- Green LED
- Yellow LED
- Red LED
- Buzzer
- Resistors
- Breadboard
- Jumper Wires

Pin Connections

Component| Arduino Pin
HC-SR04 TRIG| D9
HC-SR04 ECHO| D10
Green LED| D2
Yellow LED| D3
Red LED| D4
Buzzer| D5

Working

The HC-SR04 ultrasonic sensor sends an ultrasonic pulse and measures the time taken for the echo to return.

Arduino calculates the distance using the measured echo time.

The system then classifies the measured distance into different levels:

- 🟢 Low Distance Level → Green LED ON
- 🟡 Medium Distance Level → Yellow LED ON
- 🔴 High Distance Level → Red LED + Buzzer ON

The measured distance and status are displayed in the Serial Monitor.

Threshold Levels

The system uses a reference distance of 20 cm and converts the measured distance into a percentage-based level.

Level| Indicator
Below 35%| 🟢 Green LED
35% – 74%| 🟡 Yellow LED
75% and above| 🔴 Red LED + Buzzer

Serial Monitor

Set the Arduino Serial Monitor to:

9600 baud

Example output:

OBJECT DETECTION SYSTEM
--------------------------------
Distance: 8.52 cm | objectDist: 11.48 cm | Level: 57.40%
Status: MEDIUM DISTANCE
--------------------------------

Features

- Real-time object distance measurement
- Ultrasonic sensing
- LED-based distance indication
- Buzzer warning system
- Serial Monitor output
- Automatic sensor error handling with multiple measurement attempts

Project Structure

arduino-object-distance-monitoring/
│
├── object_distance_monitoring.ino
└── README.md

Future Improvements

- Add an LCD/OLED display
- Add multiple distance thresholds
- Add IoT connectivity
- Send distance data to a mobile application
- Add data logging and visualization

Author

Prajuktha Shetty

License

This project is open-source and can be used for educational purposes.
