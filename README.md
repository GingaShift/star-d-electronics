# STAR-D Electronics

Electronics repository for the STAR-D (Space Test of Amoeba Response - Dictyostelium) experiment developed within the ESA REXUS/BEXUS programme.

The electronics architecture is divided into several dedicated boards responsible for power conversion, experiment control, imaging, sensing, actuation and illumination.

---

# System Overview

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

<img width="506" height="544" alt="Power_Board_F" src="https://github.com/user-attachments/assets/3bb19931-7870-4751-bd9b-60637ceb65b9" />
<img width="517" height="537" alt="Power_Board_B" src="https://github.com/user-attachments/assets/734fc25d-04d1-45fc-bb6b-e249d62143c8" />


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

<img width="553" height="372" alt="Main_Board" src="https://github.com/user-attachments/assets/f9eced76-5afc-4e95-a0da-78641fbd60ae" />
<img width="674" height="326" alt="Main_Board_B" src="https://github.com/user-attachments/assets/e2433369-b1f6-4227-bd75-72e46f01ca62" />



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

- CM5 power supply

## PCB

<img width="689" height="258" alt="5V_Board_F" src="https://github.com/user-attachments/assets/2e895902-662e-4e2e-a0f2-32f97982bfbf" />
<img width="676" height="269" alt="5V_Board_B" src="https://github.com/user-attachments/assets/5922449c-3cfd-4019-a5d7-beee842c423f" />



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

<img width="145" height="122" alt="image" src="https://github.com/user-attachments/assets/8ca04cdd-d7b6-403d-b7d4-adc886789add" />


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

<img width="436" height="472" alt="M_led" src="https://github.com/user-attachments/assets/93fdad5f-bab9-434f-a5b1-119d68b2fb04" />


---

# External BME280 Board

## Purpose

Environmental monitoring outside the Pressure Vessel.

## PCB

<img width="398" height="353" alt="External_BME_F" src="https://github.com/user-attachments/assets/7a9cec90-346b-40c7-9fde-43e71c5b2e1b" />
<img width="365" height="332" alt="External_BME_B" src="https://github.com/user-attachments/assets/03dcee8e-4531-4c65-8ecc-7f400e4eee6c" />


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
