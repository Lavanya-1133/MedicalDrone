# 🚁 Autonomous Medical Delivery UAV

An autonomous UAV platform developed for medical-supply delivery to remote and underserved healthcare centres, developed during my Robotics Engineering Internship at the **IITI DRISHTI CPS Foundation, IIT Indore**.

The project focuses on integrating a UAV flight-control stack, telemetry, simulation, and a custom payload-delivery mechanism into a practical aerial healthcare-delivery platform.

---

## 📌 Project Overview

Access to healthcare in remote regions can be constrained by difficult terrain, poor road connectivity, and long transportation times. This project explores the use of autonomous UAVs for delivering essential medical supplies to remote healthcare centres.

The system combines:

- Autonomous UAV operation
- Pixhawk-based flight control
- Real-time telemetry
- Simulation and testing
- Custom payload carrier design
- Hardware-in-the-loop validation

The objective was to develop and validate a UAV prototype capable of safely carrying and delivering medical payloads while maintaining reliable communication with the ground station.

---

## 🎯 Objectives

- Develop a UAV platform for autonomous medical-supply delivery.
- Integrate the Pixhawk flight controller with the UAV architecture.
- Establish reliable real-time telemetry between the UAV and ground station.
- Design and integrate a mechanism for carrying the medical payload.
- Validate the integrated system through simulation and hardware-in-the-loop testing.
- Evaluate the platform for deployment in remote healthcare scenarios.

---

## 🏗️ System Architecture

```text
                    ┌─────────────────────┐
                    │    Mission / GCS    │
                    │   QGroundControl    │
                    └──────────┬──────────┘
                               │
                         Telemetry Link
                               │
                               ▼
                    ┌─────────────────────┐
                    │      Pixhawk        │
                    │   Flight Controller │
                    └──────────┬──────────┘
                               │
                ┌──────────────┼──────────────┐
                │              │              │
                ▼              ▼              ▼
             Motors         Sensors       Telemetry
                │
                ▼
        ┌─────────────────┐
        │      UAV        │
        │   Airframe      │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ Medical Payload │
        │    Carrier      │
        └─────────────────┘
