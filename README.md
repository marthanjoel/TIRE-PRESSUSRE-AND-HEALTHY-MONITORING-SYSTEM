# Tire Pressure & Health Monitoring System

## Project Overview

This project implements a **Tire Pressure & Health Monitoring System** using Arduino. The system indirectly monitors tire condition by observing temperature, tilt behavior, and wheel rotation. It alerts the driver using LEDs and a buzzer when abnormal or dangerous conditions are detected.

This is an **indirect TPMS (Tire Pressure Monitoring System)**, meaning tire pressure is not measured directly. Instead, sensor data is analyzed to estimate tire health.

---

## Components Used

* **Arduino Uno** – main controller
* **Temperature Sensor (e.g., LM35)** – measures tire temperature
* **Tilt Sensor** – detects sudden tilts or uneven movement
* **Hall Magnetic Sensor** – counts wheel rotations for wear estimation
* **Buzzer** – alerts the driver during critical conditions
* **3-Color LED (RGB or separate LEDs)** – indicates system status
* **Resistors (220Ω)** – for LED protection
* **Jumper wires & breadboard**

---

## System Functionality

* The **temperature sensor** monitors tire heat buildup.
* The **tilt sensor** detects bumps or unusual tire movement.
* The **Hall sensor** counts wheel rotations when a magnet passes nearby.
* The Arduino processes all sensor data and determines tire condition.

### Status Indication

* **Green LED** → Normal condition
* **Yellow LED** → Warning (tilt detected or temperature rising)
* **Red LED + Buzzer** → Critical condition (very high temperature)

---

## Pin Connections

| Component          | Arduino Pin |
| ------------------ | ----------- |
| Temperature Sensor | A0          |
| Tilt Sensor        | D2          |
| Hall Sensor        | D3          |
| Buzzer             | D8          |
| Red LED            | D9          |
| Yellow LED         | D10         |
| Green LED          | D11         |

---

## Working Principle

1. Arduino continuously reads sensor values.
2. If the tire temperature is normal and no tilt is detected, the green LED turns ON.
3. If a tilt is detected or temperature rises above the warning level, the yellow LED turns ON.
4. If the temperature reaches a critical level, the red LED turns ON and the buzzer sounds.
5. Rotation data from the Hall sensor can be used to estimate tire wear over time.

---

## Testing Procedure

* Test each sensor individually using the Serial Monitor.
* Verify LED color changes for different conditions.
* Check buzzer activation during critical temperature.
* Combine all components into one system after successful individual tests.

---

## Applications

* Vehicle safety systems
* Educational Arduino projects
* Tire health monitoring prototypes
* Automotive electronics learning

---

## Conclusion

This project demonstrates how multiple sensors can be combined to monitor tire health indirectly. It improves vehicle safety by providing early warnings and is suitable for learning embedded systems and automotive electronics.

---

**Author:** Lutwama Joel Marthan

