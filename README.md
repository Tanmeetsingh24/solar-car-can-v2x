# Solar-car CAN and V2X

**Embedded Systems Engineer · Sunswift Racing (UNSW)**

> **Public case study only** — no proprietary source, schematics, or team-confidential detail.  
> Summary of work by Tanmeet Singh Sachdeva for portfolio purposes.

---

## The hook

A solar race car needed a **coherent vehicle data backbone** and **driver-awareness comms** while the team scaled electronics across a **~75-person** program — ad hoc wiring and one-off links would not survive integration.

## High-level impact

- **CAN FD network** carrying data from **12 STAR nodes**.
- **Dash Connect** — **5G C-V2X** module for driver-awareness use cases.
- **AWS IoT Core + Grafana** live telemetry for race engineering.
- **Led two electronics projects** from concept through implementation and deployment.

## My contribution

- **Architected CAN FD** topology and integration for multi-node vehicle data.
- Developed **Dash Connect** (5G V2X) for awareness-related messaging.
- Integrated **cloud telemetry pipeline** (AWS IoT Core, Grafana dashboards).
- Coordinated interfaces, testing, and deployment within a large multidisciplinary team.

## Tech and design choices

| Choice | Why |
| --- | --- |
| **CAN FD** (vs classic CAN only) | Higher throughput for growing sensor/actuator set on a long vehicle bus. |
| **STAR node pattern** | Team-standard modules; architecture had to document IDs, rates, and failure modes clearly. |
| **5G V2X for Dash Connect** | Race context needed awareness beyond in-vehicle CAN; cellular C-V2X matched event/message model. |
| **AWS IoT Core + Grafana** | Off-car visibility for strategists/engineers without custom server ops during event weeks. |

## Lesson / twist

**Telemetry volume** and **bus load** rose together as nodes came online — fixed by **rate-limiting non-critical frames**, validating DBC/load on the bench, and separating “race-critical CAN” from “logging-heavy” paths before on-track shakedown.

---

**Context:** [Portfolio](https://tanmeetsingh24.github.io) · [Formula Student DAQ](https://github.com/Tanmeetsingh24/formula-student-daq) (prior team work).
