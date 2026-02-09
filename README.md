# Spec.Project-UI: Multi-Protocol Web HMI for Process Flow Tank

A Multi-Protocol (OPC-UA, MODBUS, MQTT) supported Web HMI development for the Control System of a Process Flow Tank using **CDP Studio**.

![Web HMI Screenshot](Images/CDP%20Studio%20Pics/WebGUI%20.png)

## Overview

This project focuses on developing a dynamic, web-based Graphical User Interface (GUI) that enables seamless communication and control for industrial automation. The system leverages the **CDP Studio** platform to interface with a Process Tank Simulator, supporting real-time data exchange across three major industrial protocols:

- **OPC-UA**: Platform-independent, service-oriented architecture for robust data modeling.
- **MQTT**: Lightweight messaging protocol optimized for IoT and low-bandwidth environments.
- **MODBUS**: Industry-standard protocol for reliable device communication (TCP/IP variant).

## Key Features

- **Dynamic Protocol Selection**: Users can switch between OPC-UA, MQTT, and MODBUS at runtime.
- **Real-Time Monitoring**: Graphical representation of tank parameters (fluid level, pressure, flow rate).
- **Process Tank Simulation**: Mathematical modeling of fluid dynamics (inflow, outflow, hydrostatic pressure).
- **Scalable Architecture**: Support for multiple tank interfaces (up to 100) managed through CDP Studio.

## System Architecture

The project utilizes a modular approach, separating the simulation logic, protocol handling, and HMI display.

![System Overview](Images/CDP%20Studio%20Pics/CDPStudioSystemOverview.webp)

### Communication Protocols

| Protocol | Purpose |
| :--- | :--- |
| **OPC-UA** | Address Space Model with Node-based access. |
| **MQTT** | Pub/Sub model for efficient telemetry. |
| **MODBUS** | Register-based addressing (Holding Registers). |

## Modeling of Process Control Tank

The simulation is based on fundamental fluid dynamics:

- **Inflow/Outflow**: Managed via discharge coefficients and time-step integration.
- **Hydrostatic Pressure**: Calculated based on fluid density and height ($P = \rho \cdot g \cdot h$).

## Technical Details

- **Platform**: CDP Studio IDE
- **Language**: C++ (Library Development), Python (Configurator API)
- **HMI Technlogy**: CDP Studio Web HMI (HTML5)

---
Developed as part of the IE505718 - Simulation and Visualization Specialization Project at NTNU.
