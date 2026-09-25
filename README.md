# arduino-water-level-monitoring
Water level monitoring system using Arduino UNO and HC-SR04 ultrasonic sensor.
Arduino Water Level Monitoring System

Overview

This project is an Arduino-based water level monitoring system using an HC-SR04 ultrasonic sensor.

The ultrasonic sensor measures the distance between the sensor and the water/object surface. The Arduino calculates the level percentage and indicates the level using three LEDs and a buzzer.

Components

- Arduino UNO
- HC-SR04 Ultrasonic Sensor
- Green LED
- Yellow LED
- Red LED
- Buzzer
- Resistors
- Jumper wires
- Breadboard

Pin Connections

Component| Arduino Pin
HC-SR04 TRIG| D9
HC-SR04 ECHO| D10
Green LED| D2
Yellow LED| D3
Red LED| D4
Buzzer| D5

Working

The HC-SR04 sends an ultrasonic pulse and receives its echo. Arduino calculates the distance using the echo time.

The project then calculates the object/water level:

Level = (Tank Height - Measured Distance) / Tank Height × 100

The tank/object height used in the program is 20 cm.

Level Indication

- Below 35% → Green LED ON
- 35%–74% → Yellow LED ON
- 75% and above → Red LED + Buzzer ON

Serial Monitor

Open the Arduino Serial Monitor and set the baud rate to:

9600 baud

The system displays the measured distance, calculated level, percentage, and warning status.

Arduino Code

The main program is available in:

"water_level_monitoring.ino"

Future Improvements

- Add an LCD/OLED display
- Add a water pump control system
- Add IoT monitoring
- Add mobile notifications
- Improve sensor error handling
