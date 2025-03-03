# 🚒 Firefighting Robot using Arduino & Flame Sensor

## 🔥 Introduction
Firefighters put their lives at risk every day to protect people and property. But what if we could automate fire detection and suppression to assist them? Enter our **Firefighting Robot**—an Arduino-powered robotic system designed to detect and extinguish fires autonomously. Equipped with a **flame sensor, water spray mechanism, and servo motors**, this robot actively fights fire by detecting flames and spraying water in the right direction. 

## 🛠️ Components Required

### 🔹 Hardware:
- **Arduino Uno**
- **USB – A to micro-USB cable**
- **Car chassis**
- **L298N Motor Driver Module**
- **Flame Sensor Module**
- **Servo Motor (MG90S)**
- **L293D Motor Driver Module**
- **Mini DC Submersible Pump**
- **12V Battery**
- **On-Off Switch**
- **DC Female Connector Jack**
- **Connecting Wires**
- **Soldering Iron & Solder Wire**
- **Hot Glue Gun**

### 💻 Software:
- **Arduino IDE**

## 🔍 Understanding the Key Components

### 🔥 Flame Sensor
- Detects fire using **Infrared (IR) and Ultraviolet (UV) detection**.
- Responds to light wavelengths between **760 nm and 1100 nm**.
- Can detect fire from **up to 100 cm** away.
- Outputs both **analog and digital signals**.

### ⚙️ Servo Motor (MG90S)
- Can rotate **90° in both directions** (total ~180° movement).
- Used to control the direction of the water spray nozzle.

### 🔌 Motor Driver (L298N)
- Used to control **two DC motors**.
- **Operating Voltage:** 5-35V.
- **Logic Voltage:** 4.5-7V.
- **Max Current:** 2A per channel.

## ⚡ Circuit Diagram & Connections
![image](https://github.com/user-attachments/assets/286f01b5-8f88-4cec-a574-202ff964f534)

### 🏎️ **L298N Motor Driver Module → Arduino**
| L298N Pins | Arduino Pins |
|------------|--------------|
| ENA        | 3            |
| IN1        | 12           |
| IN2        | 4            |
| IN3        | 7            |
| IN4        | 2            |
| ENB        | 5            |

### 🏎️ **L293D Motor Driver Module → Arduino**
| L293D Pins | Arduino Pins |
|------------|--------------|
| 12V       | 12V          |
| GND       | GND          |
| 5V        | 5V           |
| EN1       | 5V           |
| IN1       | GND          |
| IN2       | 6            |

### 🛞 **Servo Motor → Arduino**
| Servo Pins | Arduino Pins |
|-----------|--------------|
| Vcc       | 5V           |
| GND       | GND          |
| Signal    | 11           |

### 🔥 **Flame Sensor → Arduino**
| Flame Sensor Pins | Arduino Pins |
|------------------|--------------|
| Vcc             | 5V           |
| GND             | GND          |
| DO (RIGHT)      | 9            |
| DO (FORWARD)    | 8            |
| DO (LEFT)       | 10           |

⚠️ **Note:** Motors are connected to the **motor terminals** of the **L298N driver module**. The driver has three main terminals:
- **12V** → Connected to battery.
- **GND** → Connected to battery’s negative terminal **(also connected to Arduino GND)**.
- **5V** → Connected to Arduino 5V.

## 🚀 Working Principle
1. **Power ON** the robot using the **12V battery**.
2. The **Arduino Uno** receives input from the **flame sensor**.
3. If a fire is detected:
   - The **water pump** activates.
   - The **servo motor** adjusts the nozzle direction.
   - Water is sprayed towards the fire.
4. The **robot stops spraying** once the fire is extinguished.

## 🚀 Future Enhancements
✅ Use **rechargeable battery packs** for longer operational life.
✅ Add **ultrasonic sensors** (HC-SR04) for **obstacle avoidance**.
✅ Upgrade with **AI & computer vision** to detect and classify different types of fires.
✅ Implement **IoT integration** for remote monitoring and real-time alerts.
✅ Develop a **mobile app** for manual control and status tracking.

## 🎯 Conclusion
This **Firefighting Robot** is a step towards **smart automation in fire emergency response**. By using Arduino and flame sensors, we have built a **cost-effective, easy-to-assemble robot** that can detect and extinguish fires autonomously. With future upgrades, this project can contribute to real-world **IoT-based firefighting solutions**.

