# PCB-Design

This repository contains two PCB design projects, each focusing on sensor integration and signal processing. The designs were carried out using industry-standard tools and methodologies, ensuring robust performance in real-world applications.

### 1. Project 1 - Accelerometer PCB with Double LED Detection System
- **Project File:** `accelerometer-pcb-design`
- **Description:** This project involves designing a PCB for an accelerometer that utilizes a novel double LED technique to detect acceleration. The design compares light intensity variations caused by motion to measure acceleration. This approach is highly sensitive, making it suitable for detecting small positional changes.

- **Key Components:**
  - **Double LED System:** The LEDs act as optical sensors, where changes in the relative distance between them (due to acceleration) alter the received light signal. This allows for precise acceleration detection.
  - **Signal Gain:** The design incorporates a gain stage to clean and amplify the small voltage changes produced by the LEDs. A high-gain operational amplifier is used to improve the signal-to-noise ratio, ensuring accurate measurements while minimizing interference.

- **Theory Behind the Gain:**
  - Since the LED sensors produce a low output voltage, amplification is required to improve the signal-to-noise ratio. An operational amplifier is used with a gain factor determined by:
    \[
    V_{\text{out}} = A \times (V_{\text{in}} - V_{\text{ref}})
    \]
    Where \(A\) represents the amplifier’s gain and \(V_{\text{ref}}\) is the reference voltage, which stabilizes the system. Amplifying the signal enables downstream components like the ADC to measure the acceleration accurately.

---

### 2. Project 2 - Complete PCB Design with DC Motor Controller Integration
- **Project File:** `motor-controller-pcb-design`
- **Description:** This project involves the complete design of a PCB, including both the schematic and layout, to integrate various components such as a **DC motor controller**. The design aims to manage motor control for applications that require precise motion handling. The PCB integrates power management, motor control, and communication interfaces, ensuring stable and reliable performance in real-world conditions.

- **Circuit Design and Layout:**
  - **Two-Layer PCB Design**: The PCB was designed as a two-layer board to separate signal and power planes, minimizing interference. The top layer handles most of the power components, while the bottom layer is used for signal routing and communication lines.
  - **H-Bridge Layout**: The H-bridge configuration of the DC motor controller was carefully laid out to minimize resistance and power loss. Free vias were used to ensure stable ground connections and avoid issues with heat dissipation.
  - **Trace Routing**: Power traces were routed with greater width to handle higher current, while control signal traces were kept short to reduce noise. Decoupling capacitors were placed strategically close to key components to filter high-frequency noise.

- **Special Features:**
  - **Motor Direction Control**: The motor controller allows for dynamic control of motor direction by toggling the DIR pin through the microcontroller. The PCB includes dedicated pins for this purpose.
  - **PWM Speed Control**: By connecting the motor controller’s PWM input to the microcontroller, the design supports precise motor speed control. This allows the user to modulate the speed based on the application’s requirements.
  - **Overcurrent and Thermal Protection**: The motor controller includes built-in protection circuits to prevent damage from overcurrent or overheating, ensuring the durability of the design in demanding conditions.

This project focuses on delivering a reliable and efficient motor control system through meticulous PCB design, incorporating all the necessary components to handle power management, motor control, and system protection.

For more details on the design and implementation of the motor controller PCB, refer to the technical documentation included in this repository.


## Getting Started

1. **Clone the repository:**
   ```bash
   git clone https://github.com/jacopodallafior/PCB-design.git
