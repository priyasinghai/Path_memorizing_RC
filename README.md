--> Path-Memorizing RC Robot using ESP8266

A Wi-Fi controlled RC robot capable of recording, storing, and replaying its movement path.  
The robot is built using an ESP8266 NodeMCU and an L298N dual H-bridge motor driver, allowing both manual control and autonomous to-and-fro navigation based on stored motion data.

---

--> Project Overview

This project demonstrates how an embedded system can learn a path through user control, store directional commands with timing information, and later retrace the exact path autonomously.  
The robot can be driven remotely over Wi-Fi and can replay the memorized path in both forward and reverse directions.

---

--> Features

- Wi-Fi based remote control using ESP8266  
- Real-time path recording (direction + duration)  
- Autonomous path replay  
- Forward and reverse (to-and-fro) traversal  
- Differential drive control using L298N  
- Modular and extensible firmware design  

---

--> Tech Stack

-> Hardware
- ESP8266 NodeMCU  
- L298N Dual H-Bridge Motor Driver  
- DC Gear Motors  
- RC Car Chassis  
- Battery Pack  

-> Software
- Arduino IDE  
- Embedded C / Arduino Framework  
- ESP8266 Wi-Fi Libraries  

-> Communication
- Wi-Fi (HTTP-based control commands)

-> Design & Tools
- EasyEDA (PCB design)  
- SolidWorks (Mechanical modeling)

---

--> Pin Configuration

| ESP8266 Pin | L298N Pin | Function |
|------------|-----------|----------|
| D2 | IN1 | Left motor direction |
| D3 | IN2 | Left motor direction |
| D4 | IN3 | Right motor direction |
| D5 | IN4 | Right motor direction |
| D6 | ENA | Left motor speed (PWM) |
| D7 | ENB | Right motor speed (PWM) |

⚠️ Ensure a common ground between ESP8266 and L298N.

---

--> Working Principle

1. The robot is manually driven via Wi-Fi using control commands.
2. Each movement command (forward, backward, left, right) along with its execution time is stored in memory.
3. Once recording is complete, the robot switches to autonomous mode.
4. Stored commands are replayed sequentially to retrace the original path.
5. Reverse traversal is achieved by reversing the stored command sequence and directions.

---

--> Path Memorization Logic

- Commands are stored as structured data containing:
  - Direction
  - Duration
- Timing-based motion is used instead of encoders.
- Replay accuracy depends on motor consistency and battery voltage.

---



