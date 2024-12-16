# Power Automation System for Power Loom and Textile Industry

## Overview

The **Power Automation System** is an automated solution designed for controlling and monitoring power looms in the textile industry. The system is based on the **PIC18F4550 microcontroller** and is developed using **MPLAB IDE**, **XC8 Compiler**, **CCS Compiler**, and **microC** for the software. It integrates a range of industrial sensors and advanced motor control techniques to automate the loom's operations, ensuring enhanced productivity, safety, and process optimization.

## Version 1
![V1 Image](https://github.com/karthirilla/Power_Loom_Automation/blob/main/LOOM_AUTOMATION_V1.png)

## Version 2
![V2 Image](https://github.com/karthirilla/Power_Loom_Automation/blob/main/LOOM_AUTOMATION_V2.jpg)

## Version 3
![V3 Image](https://github.com/karthirilla/Power_Loom_Automation/blob/main/LOOM_AUTOMATION_V3.png)


### Key Features

- **Central Controller**: Uses **PIC18F4550** microcontroller for real-time monitoring and control.
- **AC Motor Control**: Employs **DC injection braking** for immediate motor stoppage.
- **Thread Monitoring**: Utilizes **photodiode sensors** and **proximity sensors** for thread detection (warp and weft).
- **Motor Position and Warp Count Detection**: Monitors the loom’s position and counts warp threads.
- **Industrial Standards**: Features electrical isolation using **PC817 optocouplers** and **ULN2008** driver for controlling high-load components.
- **Safety Features**: Stops the motor if any thread breaks or if the loom reaches a specified position.

## System Components

- **Microcontroller**: **PIC18F4550** for processing logic, monitoring sensors, and controlling actuators.
- **Sensors**: 
  - **Photodiode Sensors**: For detecting thread breaks (weft and warp).
  - **Industrial Proximity Sensors**: For monitoring warp count and loom position.
- **Motor Control**: 
  - **AC Motor** controlled via **12V relays** and **DC injection braking**.
  - **DC Injection Braking**: For quick stopping of the motor in case of thread breakage or loom misalignment.
- **Safety Isolation**: 
  - **PC817 Optocouplers** for electrical isolation between the microcontroller and high-voltage components.
- **Motor Driver**: **ULN2008** driver for output control to relay circuits.
- **Weft Thread Detection**: Implemented using an **LM358 operational amplifier** comparator circuit.

## Features in Detail

### 1. **Motor Monitoring and Control**
The system controls the AC motor driving the loom, ensuring that it operates at the correct speed and position. It can immediately stop the motor using the **DC injection braking** mechanism, which injects a DC current into the motor windings to halt the motor instantly.

### 2. **Thread Monitoring (Warp and Weft)**
- **Warp Thread Count**: Monitored using industrial **proximity sensors**, which track the number of threads in the loom and ensure the loom operates within the required parameters.
- **Weft Thread Cut Detection**: Utilizes an **LM358 op-amp comparator** circuit to detect if a weft thread has been cut or broken, triggering an automatic stop of the motor.

### 3. **User Interface and Control**
The system allows the user to interact with the loom via several input buttons:
- **Stop**: To halt the loom motor.
- **Run**: To start the motor.
- **Break**: To immediately stop the motor in case of emergency or thread issues.
- **Inch**: Allows precise, small adjustments to the loom’s position for fine-tuning.

### 4. **Electrical Isolation and Protection**
The system incorporates **PC817 optocouplers** to isolate the high-voltage AC components from the low-voltage control system. This prevents damage to the microcontroller and ensures safe operation. The power supply also features isolation to avoid any interference from high-voltage spikes.

### 5. **Motor Driver and Relay Control**
The **ULN2008** driver is used to interface with the **12V relays**, controlling the AC motor. The relays provide switching capabilities for high-load devices like the motor, while maintaining electrical isolation.

---

## System Workflow

1. **Startup**: Upon powering up, the system initializes sensors, motor control, and the microcontroller's logic. It checks for any user inputs and prepares the system for operation.
2. **Motor Operation**: The motor starts operating based on user input or automated instructions. It continuously monitors warp count, thread condition, and motor position.
3. **Thread Monitoring**: The sensors (photodiode and proximity sensors) monitor the loom's threads, ensuring there are no breaks or malfunctions. If any issues are detected, the system halts the motor via DC injection braking.
4. **User Interaction**: The user can manually control the system using the control buttons (**Stop**, **Run**, **Break**, **Inch**) to manage the loom's operations.
5. **Safety and Shutdown**: The system continuously monitors motor speed, thread status, and loom position. If any anomalies or thread cuts are detected, the system stops the motor immediately to avoid further damage.

---

## Circuit Diagram

A detailed circuit diagram will be included to illustrate the connections between the microcontroller, sensors, relays, and motor control systems. The diagram will highlight the use of isolation techniques and motor control interfaces.

---

## Hardware Components List

1. **PIC18F4550 Microcontroller**
2. **PC817 Optocouplers**
3. **ULN2008 Driver IC**
4. **Photodiode Sensors**
5. **Industrial Proximity Sensors**
6. **LM358 Operational Amplifier**
7. **DC Injection Braking Circuit**
8. **12V Relays**
9. **AC Motor**
10. **Power Supply Components (12V, isolated)**

---

## Software and Development Environment

- **MPLAB IDE**: Primary development environment for coding.
- **XC8 Compiler**: Compiler for PIC18F4550 code.
- **CCS Compiler**: Alternative compiler for ease of integration.
- **microC**: Used for specific software functionalities and features.

---

## Contributing

If you would like to contribute to this project, feel free to fork the repository, submit issues, or send pull requests. Any improvements, bug fixes, or new features are welcome.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgments

- Thanks to **MPLAB IDE**, **CCS Compiler**, **microC**, and the open-source community for providing great tools for embedded development.
- Special thanks to all contributors for their support and contributions to this project.

