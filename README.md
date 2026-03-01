# 🤖 IoT-Enabled ESP32 Mobile Robot for Obstacle Detection and Remote Monitoring

A comprehensive Internet of Things (IoT) mobile robot system designed to autonomously detect and avoid obstacles while providing continuous remote monitoring capabilities. Built on the **ESP32** microcontroller, this project integrates hardware sensors, local decision-making logic, and cloud-based analytics.

---

## 🔗 Project Links
* **Live Simulation**: [Wokwi Virtual Prototype](https://wokwi.com/projects/450946223071784961)

---

## 🎯 Project Goals & Objectives

* **🛡️ Autonomous Navigation**: Implement real-time obstacle detection for safe movement in various environments.
* **☁️ Remote Monitoring**: Enable continuous tracking of sensor data, battery life, and robot status via a cloud dashboard.
* **🔋 Power Management**: Optimize energy efficiency through periodic cloud updates and a low-battery safe mode.
* **🔒 Secure Data Transmission**: Ensure safe telemetry uploads using private channels and API key authentication.

---

## 🛠️ Hardware & Tech Stack

### **Core Hardware**
* **Microcontroller**: ESP32 (Features built-in Wi-Fi and low power consumption).
* **Proximity Sensing**: HC-SR04 Ultrasonic Sensor (Measures distance to front-facing obstacles).
* **Indicators**: LEDs to represent robot states (Green = Forward, Red = Stop, Yellow = Warning).
* **Power Monitoring**: Potentiometer connected to the ESP32 ADC pin to simulate and monitor battery voltage.

### **Software & Cloud**
* **Programming**: C++ / Arduino IDE.
* **Simulation**: Wokwi Virtual Prototyping.
* **Cloud Platform**: ThingSpeak Cloud (HTTP Protocol).

---

## 🧠 System Architecture & Decision Logic

The robot operates on a distinct flow of sensor reading, decision logic, actuation, and cloud communication.

1. **Battery Check**: The system first reads the battery level via the ADC. If the battery is low, the robot enters "Safe Mode," stops movement, and activates the warning indicator.
2. **Obstacle Detection**: If power is sufficient, the HC-SR04 sensor checks the distance to the nearest object. 
3. **Actuation**: If an obstacle breaches the safe threshold, the robot halts (Red LED). If the path is clear, it moves forward (Green LED).
4. **Cloud Sync**: To conserve power, telemetry data (distance, robot state, battery percentage, and low-battery alerts) is transmitted to ThingSpeak every 15 seconds over Wi-Fi.

---

## 👥 Developer Information

This project was developed for the **Internet of Things (IoT) - CDE2243** course at the School of Computing and Informatics.

* 👤 **Abdulrahman Omar Abobakr Alamodi**
* 👨‍🏫 **Instructor**: Ts. Mohd Zulkifli Mohd Zaki
