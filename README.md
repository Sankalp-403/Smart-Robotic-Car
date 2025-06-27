# 🤖 Smart Robotic Car (Obstacle Avoidance + Bluetooth + Voice Control)

This is an Arduino-based smart robotic car that can navigate autonomously by avoiding obstacles, or be controlled manually via **Bluetooth** or **voice commands**. It uses **ultrasonic sensors**, **servo motors**, and **AFMotor shield** to move intelligently and safely.

---

## 🚗 Features

- **Autonomous Obstacle Avoidance**  
  Uses an ultrasonic sensor mounted on a servo to detect obstacles in front and intelligently decide to turn left or right.

- **Bluetooth Control**  
  Accepts directional commands from a smartphone via Bluetooth (e.g., using a Bluetooth terminal app).

- **Voice Command Control**  
  Supports voice-controlled navigation through symbol-based commands sent over serial (with a voice assistant or app).

- **Modular Design**  
  Easily switch between obstacle, Bluetooth, and voice control by commenting/uncommenting functions in the main loop.

---

## 🧠 Hardware Components

- Arduino Uno
- HC-SR04 Ultrasonic Sensor
- SG90 Servo Motor
- HC-05 / HC-06 Bluetooth Module
- L298P Motor Driver (AFMotor Shield)
- 4x DC Motors
- Chassis and wheels
- 9V Battery or Power Bank

---

## 🛠️ How It Works

### Control Modes:
- **Obstacle Avoidance**: Car scans and chooses the direction with more space when it detects an obstacle closer than 12 cm.
- **Bluetooth**: Receives characters like `'F'`, `'B'`, `'L'`, `'R'`, `'S'` to move.
- **Voice**: Interprets symbols like `^`, `<`, `>`, `*` for directions.

### Commands Overview:

| Mode      | Command | Action        |
|-----------|---------|---------------|
| Bluetooth | F       | Forward       |
|           | B       | Backward      |
|           | L       | Turn Left     |
|           | R       | Turn Right    |
|           | S       | Stop          |
| Voice     | ^       | Forward       |
|           | -       | Backward      |
|           | <       | Turn Left     |
|           | >       | Turn Right    |
|           | *       | Stop          |

---

## 📂 File Structure

SmartRoboticCar/
├── SmartRoboticCar.ino # Main Arduino sketch
└── README.md # This documentation


---

## 🔌 Setup Instructions

1. Upload the code to the Arduino Uno.
2. Power the circuit using a 9V battery or USB.
3. Choose control mode by enabling one of the following in `loop()`:
   ```cpp
   //Obstacle();
   //Bluetoothcontrol();
   //voicecontrol();
4.Connect your Bluetooth device (if used) and test with a terminal app or voice assistant.




![image](https://github.com/user-attachments/assets/64633ea3-5348-4ba2-a65a-a77142fe3bcf)



