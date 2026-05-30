# STAR-D Electronics

Electronics repository for the STAR-D (Space Test of Amoeba Response - Dictyostelium) experiment developed within the ESA REXUS/BEXUS programme.

The electronics architecture is divided into several dedicated boards responsible for power conversion, experiment control, imaging, sensing, actuation and illumination.

---

# System Overview

![Global Architecture](Documentation/Images/Global_Architecture.png)

The STAR-D electronics system is organized around:

- Power Board
- Main Control Board
- 5V Distribution Board
- CM5 Imaging System
- Microscope LED Board
- External Sensor Interfaces

---

# Power Board

## Purpose

Interfaces directly with the REXUS Service Module.

Responsibilities:

- 28V input from REXUS
- Power conversion
- Signal isolation
- RS422 communications
- Power distribution to the experiment

## PCB

![Power Board](Documentation/Images/Power_Board.png)

## Main Components

- DC/DC Converters
- Optocouplers
- RS422 Transceiver
- D-SUB Interface
- Protection circuitry

---

# Main Control Board

## Purpose

Central controller of the experiment.

Responsibilities:

- Sensor acquisition
- Heater control
- Fluidic control
- Experiment sequencing
- Telemetry generation

## PCB

![Main Board](Documentation/Images/Main_Board.png)

## Main Components

- ESP32-S3
- MAX31865
- PT100 Interface
- LSM6DSM
- ABP Pressure Sensor Interface
- SLF3S Flow Sensor Interface
- Actuator Drivers

---

# 5V Distribution Board

## Purpose

Dedicated power distribution board for high-current 5V subsystems.

Responsibilities:

- Heater power distribution
- CM5 power supply
- LED power distribution

## PCB

![5V Board](Documentation/Images/5V_Board.png)

---

# CM5 Imaging System

## Purpose

Scientific image acquisition and storage.

Responsibilities:

- Microscope control
- Camera acquisition
- Data storage
- Image processing

## PCB

![CM5 Board](Documentation/Images/CM5_Board.png)

## Main Components

- Raspberry Pi CM5
- NVMe SSD
- CSI Camera Interface

---

# Microscope LED PCB

## Purpose

Microscope illumination.

Responsibilities:

- Brightfield illumination
- Fluorescence illumination

## PCB

![Microscope LED PCB](Documentation/Images/Microscope_LED_PCB.png)

---

# External BME280 Board

## Purpose

Environmental monitoring outside the Pressure Vessel.

## PCB

![External BME280](Documentation/Images/BME280_External.png)

---

# Repository Structure

```text
Documentation/
├── SED
├── Part_Listing
├── ICD
└── Images

Power_Board/

Main_Board/

5V_Board/

CM5_System/

Microscope_LED_PCB/

BME280_External/
```

---

# Documentation

Useful documents:

- STAR-D SED
- REXUS ICD
- Global Part Listing
- Power Board Part Listing
- Test Reports
- Integration Documents

---


# Team

STAR-D Electronics Team

Electronic Lead:
**Eden Elfassy**

ESA REXUS/BEXUS Programme
