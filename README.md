# 🚗 CAN-Based Interior Light & Seat Belt Warning System

A CAN-based automotive embedded system demonstrating communication between multiple Electronic Control Units (ECUs) for interior light control, seat belt monitoring, and dashboard status indication.

The project models a small automotive CAN network using multiple ECU nodes, a CAN database, message handling, timer handling, Signal Watch, and Signal Graph analysis.

---

## 📌 Project Overview

Modern vehicles contain multiple Electronic Control Units (ECUs) that communicate with each other over in-vehicle networks.

This project demonstrates a simplified automotive CAN network consisting of:

- ABS ECU
- BMS ECU
- Dashboard ECU

Vehicle information is represented using CAN database signals and transmitted between the ECU nodes.

The dashboard ECU receives relevant information and provides status information such as door condition and seat belt status.

---

## 🎯 Objectives

- Understand the fundamentals of CAN communication.
- Create and configure a CAN database.
- Define automotive signals and messages.
- Create multiple ECU nodes.
- Implement timer handlers and message handlers.
- Monitor CAN signals in real time.
- Analyze CAN signal behavior using graphical visualization.
- Understand ECU-to-ECU communication in automotive systems.

---

## 🧠 System Concept

The project uses a simplified automotive CAN network.

```text
                 ┌─────────────────┐
                 │    ABS_ECU      │
                 │                 │
                 │ CAN Messages    │
                 └────────┬────────┘
                          │
                          │
                    ┌─────▼─────┐
                    │  CAN BUS  │
                    └─────┬─────┘
                          │
             ┌────────────┴────────────┐
             │                         │
      ┌──────▼──────┐           ┌──────▼─────────┐
      │   BMS_ECU    │          │ dash_board_ECU │
      │              │          │                │
      │ CAN Messages │          │ Status Display │
      └──────────────┘          └────────────────┘
```
---

## 🚌 CAN Database

A CAN database was created to define the messages and signals used by the vehicle network.

Important signals include:

| Signal             | Purpose                          |
| ------------------ | -------------------------------- |
| `Door_status`      | Represents door status           |
| `seat_belt_Status` | Represents seat belt status      |
| `dashboard_msg`    | Dashboard-related message/status |

The database provides a structured definition of the CAN communication between the ECU nodes.

---

## 🔌 ECU Nodes

Three ECU nodes were created for the automotive network.

### 1. ABS_ECU

Represents the Anti-lock Braking System ECU and participates in CAN message communication.

### 2. BMS_ECU

Represents the Battery Management System ECU and communicates vehicle-related information through the CAN network.

### 3. dash_board_ECU

Receives CAN information and represents the dashboard-side processing of vehicle status information.

---

## ⚙️ Message & Timer Handling

Timer handlers and message handlers were implemented for the ECU nodes.

The timer-based mechanism allows periodic CAN communication, while message handlers process received CAN messages.

```
Timer Event
     │
     ▼
Generate / Transmit CAN Message
     │
     ▼
CAN BUS
     │
     ▼
Receive Message
     │
     ▼
Message Handler
     │
     ▼
Update Vehicle Signal
```
---

## 📊 Signal Monitoring

The CAN signals were monitored using the Signal Watch functionality.

Signal Watch allows the current values of database-defined signals to be observed during simulation.

Example signals:
```
Door_status
seat_belt_Status
dashboard_msg
```
---

## 📈 Signal Graph

Signal Graph was used to visualize signal behavior over time.

<img width="1902" height="776" alt="Signal Graph" src="https://github.com/user-attachments/assets/4b0baaca-9a57-4111-8a22-2300f0dac0f0" />

This makes it possible to observe changes in vehicle signals during CAN communication and simulation.

---

## 🛠️ Tools & Technologies
- CAN
- CAN Bus
- Automotive ECU Communication
- CAN Database
- CAPL
- CANoe
- Message Handlers
- Timer Handlers
- Signal Watch
- Signal Graph

---

## 🧩 Project Workflow
```
Create CAN Database
        │
        ▼
Define Messages & Signals
        │
        ▼
Create ECU Nodes
        │
        ▼
Implement Timer Handlers
        │
        ▼
Implement Message Handlers
        │
        ▼
Run CAN Simulation
        │
        ▼
Monitor Signals
        │
        ▼
Analyze Signal Graphs
```
---

## 🚀 Learning Outcomes

Through this project, I gained practical experience with:

- CAN bus fundamentals
- Automotive communication architecture
- ECU-based network design
- CAN database configuration
- CAN message and signal handling
- Timer-based communication
- Real-time signal monitoring
- CAN network debugging and visualization
- Automotive embedded-system concepts

---

## 🔮 Future Improvements

Possible extensions include:

Add CAN error handling
Implement CAN message filtering
Add additional vehicle ECUs
Add diagnostic communication
Implement UDS-based diagnostics
Add fault injection and error simulation
Interface the CAN network with real CAN hardware
Develop a physical automotive CAN test bench

---

## 👨‍💻 Author

Chinmay N. Yalawatti

Electronics & Communication Engineering

KLE Technological University, BVB Campus
