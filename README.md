# -EV-Wireless-Charging-System
🔋 EV Wireless Charging System

This project demonstrates a wireless power transfer system for Electric Vehicle (EV) charging using inductive coupling. The system includes a transmitter and receiver coil with an optimized coil shape to improve magnetic coupling efficiency and ensure safe, contactless power delivery. Controlled by an Arduino UNO, it incorporates real-time alignment detection using a Hall Effect sensor for enhanced safety and automation.

🚀 Key Features

⚡ Inductive Charging
Enables contactless energy transfer between the transmitter and receiver coils using electromagnetic fields, eliminating the need for physical connectors.

🧠 Microcontroller-Based Control
The system is powered by an Arduino UNO, which acts as the central control unit to manage sensor input and charging behavior.

🔁 Smart Power Control

Relay Module is used for automatically switching charging ON or OFF

Hall Effect Sensor checks the alignment between coils and only allows charging when coils are properly aligned

🛡️ Efficiency & Safety
Charging activates only when perfect alignment is detected, minimizing energy loss and preventing unsafe charging conditions.

🛠 Technologies Used

Arduino UNO – Microcontroller for control logic

Hall Effect Sensor – Detects coil alignment

Relay Module – Switches charging circuit ON/OFF

Transmitter Coil – Sends power wirelessly

Receiver Coil – Receives power from the transmitter

Basic Electronics – Resistors, jumper wires, breadboard, connectors, etc.

📦 Applications

🚗 Wireless EV Charging Stations – Safe, weatherproof, and maintenance-free EV charging

🏠 Smart Garage Charging – Ideal for home charging without cables

🌱 Clean and Efficient Infrastructure – Reduces wear and tear from physical connectors and promotes sustainability

💡 How It Works

Power is supplied to the transmitter coil, creating an electromagnetic field

The receiver coil, placed on the EV side, picks up this energy through inductive coupling

The Hall Effect sensor detects whether the coils are properly aligned

The Arduino processes this data:

If aligned → Activates the relay to start charging

If misaligned → Charging is prevented to avoid inefficiency or risk

📁 Repository Contents

📂 EV-Wireless-Charging/
├── code/
│ └── ev_charging.ino – Arduino source code
├── images/
│ └── system_diagram.png – Visual diagram of the setup
├── README.md – Project documentation
