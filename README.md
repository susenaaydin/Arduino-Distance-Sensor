# Arduino-Distance-Sensor
# Ultrasonic Distance Sensor – Arduino

An Arduino-based distance detection project using an **HC-SR04 ultrasonic sensor**, RGB LEDs, and a buzzer.

The system measures the distance to an object and provides visual and audible feedback based on the detected distance.

## Features

* 📏 Measures object distance using an ultrasonic sensor
* 🟢 Green LED indicates a safe distance
* 🟡 Red + green LEDs indicate a warning distance
* 🔴 Red LED and buzzer indicate a critical distance
* 📟 Displays distance measurements through the Serial Monitor
* 🔄 Continuously monitors the detected distance

## Distance-Based Alerts

| Distance | LED Status     | Buzzer |
| -------- | -------------- | ------ |
| > 30 cm  | 🟢 Green       | Off    |
| 11–30 cm | 🟡 Red + Green | Off    |
| ≤ 10 cm  | 🔴 Red         | On     |

## Hardware

* Arduino
* HC-SR04 Ultrasonic Sensor
* Red LED
* Green LED
* Blue LED
* Buzzer
* Resistors
* Breadboard
* Jumper wires

## Pin Configuration

| Component          | Arduino Pin |
| ------------------ | ----------: |
| Blue LED           |           2 |
| Red LED            |           3 |
| Green LED          |           4 |
| Buzzer             |           6 |
| Ultrasonic Trigger |          12 |
| Ultrasonic Echo    |          11 |

## How It Works

The ultrasonic sensor continuously measures the distance to the nearest object.

The `NewPing` library is used to communicate with the ultrasonic sensor and calculate the detected distance.

The measured distance is then evaluated using predefined thresholds:

```text
Distance > 30 cm
        ↓
   Green LED

10 cm < Distance ≤ 30 cm
        ↓
 Red + Green LEDs

Distance ≤ 10 cm
        ↓
 Red LED + Buzzer
```

The current distance is also printed to the Serial Monitor at **9600 baud**.

Example:

```text
Ping: 45cm
Ping: 27cm
Ping: 8cm
```

## Technologies

* **Arduino**
* **C/C++**
* **HC-SR04 Ultrasonic Sensor**
* **NewPing Library**
* **Digital I/O**
* **Serial Communication**

## Project Purpose

The purpose of this project is to practice distance measurement and hardware interaction with Arduino.

The project demonstrates:

* Ultrasonic distance measurement
* Sensor data processing
* Conditional control logic
* LED control
* Buzzer control
* Serial Monitor output
* Using external Arduino libraries

## Project Status

**Completed**

## Future Improvements

* Add an LCD or OLED display
* Use an RGB LED for smoother status indication
* Add adjustable distance thresholds
* Create different buzzer patterns based on distance
* Add multiple warning levels
* Display distance in real time on a graphical interface

## Author

**Sude Sena Aydın**
