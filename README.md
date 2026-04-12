## This repository contains the official documentation of Team "Los Grises Jr" for the Future Engineers category at the World Robot Olympiad 2026.

<p align="center">
  <img src="https://github.com/user-attachments/assets/6422e0d6-8cc2-4bbc-beaf-4bbada98c140" width="700" />
</p>

---

##  Team Members

### **Mateo Vásquez**  
**Role:** Electronics Specialist

**Age:** 14
---
### **Ruth García**  
**Role:** Builder

**Age:** 15
---
### **Renato Medina**  
**Role:** Programmer

**Age:** 14
---
##  Project Overview
---
This project presents the development of an autonomous vehicle designed for the Future Engineers category of the World Robot Olympiad 2026.

The robot is capable of navigating a dynamic environment using a combination of computer vision and closed-loop control systems.

The system integrates:

Real-time vision processing
Ackermann steering geometry
PID-based control

This combination enables stable, precise, and adaptive navigation.


##  **Robot Description**

The robot is built using an Ackermann steering system, similar to real-world vehicles.

The vehicle is based on an Ackermann steering system, similar to real-world cars.

🔧 Why Ackermann Steering?

Compared to differential drive systems, Ackermann steering provides:

Reduced lateral wheel slip
Improved curve accuracy
More realistic motion behavior
Greater stability at higher speeds

A dedicated motor controls the steering angle, allowing fine adjustments during navigation.
---
## Vehicle Photo

<div align="center">

| Front | Back |
|:--:|:--:|
|<img src= "https://github.com/user-attachments/assets/6dc00e73-723c-4a87-8fed-caf3bb0b516d" width="300"/> | <img src="https://github.com/user-attachments/assets/db47e1fc-15cf-4bf6-9bda-90c15ac27a30" width="300"/> |
| Bottom | Left |
| <img src="https://github.com/user-attachments/assets/adfcbc35-594a-4e53-b164-27f303c28fb5" width="300"/> | <img src= "https://github.com/user-attachments/assets/e4b8b09b-9287-48da-9303-3b7f5d03bd47" width= 300 /> |
| Right | Top |
|<img src= "https://github.com/user-attachments/assets/afbd04f9-7306-40f3-8b8c-13dbfa76661c" width= 300 /> | <img src= "https://github.com/user-attachments/assets/d506e87b-5d23-4b30-8219-bd6e11727323"  width= 300 /> |
---
##  Components and Hardware
| Component | Description | Image |
|-----------|-------------|-------|
| **45544 LEGO MINDSTORMS Education EV3 Core Set** | Forms the foundational structure and chassis. | <img src="https://github.com/user-attachments/assets/a725c977-b28b-4b5d-b95c-506c84cd6706" width="300"> |                       
| **Arduino Nano** | ATmega328-based microcontroller for control tasks. | <img src="https://github.com/user-attachments/assets/22e8f59c-909d-4ff2-b637-dc03e15f4de6" width="200"> |
| **DFRobot HuskyLens AI Camera** | AI-powered vision sensor capable of detecting colors, objects, and patterns in real time. | <img src="https://github.com/user-attachments/assets/fc513a62-31dd-4e8b-9117-27c28bc85ab0" width="200"> |
---

##  Strategy

The robot uses vision-based detection to identify red and green pillars and determine its path.

Based on the detected color, the robot dynamically adjusts its trajectory using the steering system, ensuring precise alignment and smooth navigation around obstacles.

The combination of computer vision and Ackermann steering allows efficient and stable autonomous performance during the competition.
---
## **Vision System**

The robot uses a HuskyLens AI camera connected to an Arduino Nano.

Capabilities:
Detection of red and green pillars
Real-time object tracking
Position data extraction
Design Considerations:
Elevated camera placement increases field of view
Early detection improves reaction time
Reduces sudden corrections
---
## **Control System Architecture**

1. Vision Processing (Arduino Nano)
Receives data from HuskyLens
Extracts object position and color
Sends processed data to EV3
2. Motion Control (EV3)
Receives processed data
Controls:
Steering motor
Drive motor
---
| **Data Flow** |
|---------------|
|HuskyLens → Arduino Nano → EV3 → Motors|


A custom PCB was developed to:

-Improve connection stability
-Reduce wiring complexity
-Increase reliability during runs
---
## Navigation Strategy

The robot uses a vision-based navigation strategy:

Detect a colored pillar
Determine its horizontal position
Calculate steering correction
Navigate around the obstacle
Behavior Logic:
Object centered → move forward
Object left → steer left
Object right → steer right

If no object is detected:

The robot continues using the last known steering value temporarily
## Steering Control (PID)

To achieve stable and precise steering, a PID controller is used.
---
## Control Objective
The robot follows a vision-based navigation algorithm:

Algorithm:
-Capture frame from HuskyLens
-Detect object color (red/green)
-Get horizontal position of the object
-Compute error
-Apply PID correction
-Adjust steering angle
-Move forward
-Behavior Logic:
-Object centered → move forward
-Object left → steer left
-Object right → steer right

If no object is detected:

The robot temporarily maintains the last steering value
---
 ## **Tuning Process**
---
To achieve smooth and stable steering, a PID controller is implemented.

**Control Objective:**

Minimize the horizontal deviation between the detected object and the center of the image.

Where:

Kp → Proportional gain (responsiveness)
Ki → Integral gain (eliminates steady-state error)
Kd → Derivative gain (reduces oscillations)
---

## Performance 

The system achieved:

Improved trajectory stability
Reduced oscillations in curves
Faster response to object position changes
Reliable navigation in dynamic environments
## **Custom PCB:**

A custom PCB was developed to:

Improve connection stability
Reduce wiring complexity
Increase reliability during competition
---
## **Challenges**
---
Integrating EV3 and Arduino systems
Achieving stable Ackermann steering control
Managing noise and variability in vision detection
Tuning PID parameters for different speeds
---
### Conclusion
---
**The Los Grises Jr robot integrates:**

Realistic Ackermann steering
Intelligent vision processing
Advanced PID control

This combination allows the robot to achieve stable, precise, and adaptive navigation, making the team was ready for every obstacle.
