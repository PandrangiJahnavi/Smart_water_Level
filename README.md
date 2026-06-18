# Smart Water Level Monitoring and Pump Automation System using ESP32, HC-SR04, and Blynk

## Overview

This project is an IoT-based Smart Water Level Monitoring and Pump Automation System developed using ESP32, HC-SR04 Ultrasonic Sensor, Relay Module, and Blynk IoT Cloud Platform.

The system continuously monitors the water level inside a tank, calculates the water level percentage, and displays real-time data on the Blynk dashboard. Based on predefined thresholds, the system automatically controls a water pump and sends instant notifications to the user.

## Features

* Real-time water level monitoring
* Automatic pump control using relay
* Blynk cloud dashboard integration
* Mobile notifications and alerts
* Water level percentage calculation
* Sensor failure detection
* LED status indication
* Remote monitoring from anywhere

## Components Required

* ESP32 Development Board
* HC-SR04 Ultrasonic Sensor
* Relay Module
* Water Pump (or relay load)
* LED Indicator
* Breadboard
* Jumper Wires
* Blynk IoT Account

## Pin Connections

| Component    | ESP32 Pin |
| ------------ | --------- |
| HC-SR04 TRIG | GPIO 13   |
| HC-SR04 ECHO | GPIO 12   |
| Relay IN     | GPIO 4    |
| LED          | GPIO 32   |
| VCC          | 5V        |
| GND          | GND       |

## Blynk Dashboard Configuration

| Virtual Pin | Function                   |
| ----------- | -------------------------- |
| V0          | Water Level Percentage (%) |
| V1          | Distance (cm)              |
| V2          | Pump/Relay Status          |

## Working Principle

1. The HC-SR04 measures the distance from the sensor to the water surface.
2. The ESP32 calculates the water level percentage.
3. The values are uploaded to the Blynk cloud dashboard.
4. When the water level exceeds 80%, the relay and LED are activated.
5. When the tank level falls below 5%, an empty tank alert is generated.
6. If the sensor fails to return an echo signal, a sensor failure notification is sent.
7. Users can monitor tank status remotely using the Blynk mobile application.

## Alert Conditions

### High Water Level Alert

Condition:

```text
Water Level ≥ 80%
```

Action:

* Relay ON
* LED ON
* Notification sent to Blynk

### Tank Empty Alert

Condition:

```text
Water Level ≤ 5%
```

Action:

* Relay OFF
* LED OFF
* Empty tank notification sent

### Sensor Failure Alert

Condition:

```text
No Echo Received
```

Action:

* Relay OFF
* LED OFF
* Sensor failure notification sent

## Serial Monitor Output

### Normal Operation

```text
[INFO] Distance: 35 cm | Level: 65 %
```

### High Water Level

```text
[INFO] Distance: 10 cm | Level: 90 %
```

### Tank Empty

```text
[INFO] Distance: 98 cm | Level: 2 %
```

### Sensor Failure

```text
[WARN] No echo — sensor failure or out of range
```

## Applications

* Smart Water Tank Monitoring
* Industrial Liquid Level Monitoring
* Agricultural Water Management
* Smart Home Automation
* Reservoir Monitoring
* Industrial IoT Systems

## Technologies Used

* ESP32
* HC-SR04 Ultrasonic Sensor
* Blynk IoT Platform
* Wi-Fi Communication
* Arduino IDE
* Embedded C/C++

## Future Enhancements

* ThingSpeak Cloud Integration
* AWS IoT Core Integration
* Historical Data Analytics
* SMS and Email Notifications
* Voice Assistant Integration
* Multiple Tank Monitoring
* Solar Powered Operation

## Project Level

### Level 1

Water level sensing using HC-SR04.

### Level 2

Cloud monitoring using Blynk Dashboard.

### Level 3

Automatic pump control with intelligent notifications and fault detection.

OUTPUT
https://github.com/PandrangiJahnavi/Smart_water_Level/blob/main/Screenshot%202026-06-15%20203851.png
https://github.com/PandrangiJahnavi/Smart_water_Level/blob/main/Screenshot%202026-06-18%20104103.png
https://github.com/PandrangiJahnavi/Smart_water_Level/blob/main/WhatsApp%20Image%202026-06-18%20at%2010.39.27%20AM%20(1).jpeg
https://github.com/PandrangiJahnavi/Smart_water_Level/blob/main/WhatsApp%20Image%202026-06-18%20at%2010.39.27%20AM%20(2).jpeg
https://github.com/PandrangiJahnavi/Smart_water_Level/blob/main/WhatsApp%20Image%202026-06-18%20at%2010.39.27%20AM%20(3).jpeg
https://github.com/PandrangiJahnavi/Smart_water_Level/blob/main/WhatsApp%20Image%202026-06-18%20at%2010.39.27%20AM.jpeg

## Author

**Pandrangi Jahnavi**

B.E. Electronics and Communication Engineering (ECE)

IoT | Embedded Systems | Cloud Computing | Industrial IoT Enthusiast
