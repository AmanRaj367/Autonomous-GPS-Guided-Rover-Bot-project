# Autonomous-GPS-Guided-Rover-Bot-project

> A group project submitted under the guidance of **TA Pallav Sir**, this autonomous rover bot leverages GPS and magnetometer-based navigation to move toward a target location without manual intervention.

## 🔍 About the Project

This project is a GPS-based autonomous rover bot designed to navigate towards predefined GPS coordinates using real-time location tracking and orientation correction. The system is built around an **ESP32 microcontroller**, **NEO-6M GPS module**, **magnetometer**, and **DC motors** controlled via a motor driver. 

The rover calculates its heading and adjusts its path continuously based on the difference between the target bearing and current orientation. Future enhancements include obstacle avoidance and RTK-level GPS accuracy.

---

##  Objectives

- Navigate autonomously to a set of GPS coordinates.
- Determine direction using a magnetometer for heading calculation.
- Correct trajectory in real-time using motor control logic.
- Tackle hardware integration and signal accuracy challenges in embedded systems.

---

##  Working Principle

1. **Initialization**: Set up GPS, magnetometer, motors, and communication protocols (UART, I2C).
2. **Position Acquisition**: NEO-6M receives GPS signals and ESP32 parses the NMEA data.
3. **Bearing Calculation**: The ESP32 calculates the required bearing to the destination using trigonometric functions.
4. **Heading Detection**: The magnetometer determines the current heading of the bot.
5. **Decision-Making**: Based on heading error, the ESP32 commands the bot to go straight, turn left, or turn right.
6. **Navigation Loop**: Continuous updates to GPS and heading allow dynamic corrections until destination is reached.
7. **Error Handling**: In case of unreliable GPS, fallback measures like hardcoded coordinates or halting are used.

---

##  Components Used

| Component             | Purpose                              |
|-----------------------|--------------------------------------|
| ESP32 (Wrover/Wroom)  | Central controller (WiFi + BT + I/O) |
| NEO-6M GPS Module     | Fetches current location data        |
| Magnetometer (e.g., HMC5883L) | Determines orientation         |
| L298N Motor Driver    | Drives left and right motors         |
| DC Motors (2)         | Controls movement                    |
| Power Supply / USB    | Supplies power                       |
| Chassis + Wheels      | Physical structure and mobility      |

---

## 🛠 Software Tools

- **Arduino IDE** – Coding and flashing firmware
- **TinyGPS++ Library** – GPS data parsing
- **Wire.h** – I2C communication with magnetometer
- **Serial Monitor** – Debugging and output display
- **GitHub** – Version control and project sharing

---

##  Development Timeline

### Week 1: Planning and Testing
- Component-level testing of ESP32, GPS
- Circuit diagram design
- Magnetometer integration

### Week 2: Code and Assembly
- Code development from pseudocode
- Hardware connections
- Encountered issues: faulty motor driver, ESP32 power inconsistency

### Week 3: Troubleshooting
- GPS issues resolved by switching to ESP32 Wroom and using spare GPS + magnetometer
- Successful integration for final video

---

## ⚙ Circuit Diagram Summary

- **GPS TX/RX ↔ ESP32 RX/TX**
- **Magnetometer SCL/SDA ↔ ESP32 I2C GPIOs**
- **Motor Driver ↔ ESP32 digital pins**
- **Motors ↔ Motor Driver outputs**

---

##  Applications

- **Precision Agriculture**: Autonomous navigation for farm vehicles
- **Warehousing**: Material movement bots
- **Surveillance**: Border patrolling with autonomous control
- **Mining**: Remote terrain exploration
- **Disaster Management**: Bots for hazardous zone entry

---

##  Challenges Faced

| Challenge                                | Solution                                           |
|------------------------------------------|----------------------------------------------------|
| Faulty motor driver                      | Replaced or worked around with limited output pins |
| Inconsistent GPS readings                | Switched ESP32 and GPS module                      |
| Power supply issues with ESP32           | Used USB/laptop instead of standalone battery      |

---

##  Future Scope

- Integration of **obstacle detection** (ultrasonic, LiDAR)
- Use of **RTK-GPS** for higher location precision
- Remote tracking and mobile UI for live rover location
- Battery-powered outdoor navigation

---

##  Team Members

- Aman Raj (2023EEB1183)  
- Ansh Singh (2023EEB1186)  
- Jaskirat Singh (2023EEB1212)  
- Vipul Kumar Singh (2023EEB1254)  
- Yashraj Omar (2023EEB1258)

---

##  Conclusion

This project demonstrates a successful implementation of autonomous navigation using GPS and magnetometer data on a budget-friendly microcontroller platform. Despite hardware limitations and signal challenges, the rover achieved its core objective — navigating towards a GPS target without manual control.

---

##  Author name
- Aman Raj
- Github : AmanRaj367

---

