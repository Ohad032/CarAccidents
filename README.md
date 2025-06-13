---
title: "README - CarsAccidentsData.csv"
output: html_document
---

## Dataset Overview

- **Filename**: `CarsAccidentsData.csv`  
- **Observations**: Each row represents a vehicle involved in a crash. Crashes with multiple vehicles appear in multiple rows.  
- **Variables**: The dataset contains 35 columns, categorized into:

  - Vehicle specifications  
  - Crash characteristics  
  - Pre-crash events  
  - Driver and environmental conditions  
  - Safety systems

## Variable Groups and Descriptions

### Vehicle Information

- `VPICMAKENAME`, `VPICMODELNAME`, `MOD_YEAR` – Make, model, and year of manufacture.  
- `BODY_STYLE` – Vehicle body type (e.g., SUV, 4 DR, 2 DR, PU/CC).

### Crash Characteristics

- `SERIAL_CRASH` – Unique identifier of the crash incident.  
- `HARM_EV`, `HARM_EVNAME` – First harmful event code and its description.  
- `TYPE_OF_COLLIOSION` – Collision type (e.g., Angle, Front-to-Rear).  
- `TRAV_SP` – Vehicle speed at the time of crash (in mph).  
- `VSPD_LIM` – Posted speed limit at the crash location (in mph).  
- `DEFORMEDNAME` – Level of damage to the vehicle.  
- `DEATHS` – Number of fatalities in the vehicle.

### Driver and Licensing

- `IS_DRIVER_PRESENT` – Indicates whether a driver was present (1 = Yes).  
- `DR_DRINK` – Indicates whether the driver consumed alcohol (1 = Yes).  
- `L_TYPENAME` – Type of driver’s license (e.g., Full Driver License).  
- `L_STATUSNAME` – License status (e.g., Valid, Suspended).  
- `SPEEDRELNAME` – Relation to speed limit (e.g., Exceeded Speed Limit).

### Environmental Conditions

- `VSURCONDNAME` – Road surface condition (e.g., Dry).  
- `MONTH`, `HOUR` – Month (1–12) and hour (0–23) of the crash.

### Pre-Crash Events

- `P_CRASH1NAME` to `PCRASH5NAME` – Sequence of events prior to the crash (e.g., Turning Left, Departed Roadway).

### Safety Features

All safety feature fields use the following coding:
- `0 = No`
- `1 = Yes`
- `2 = Unknown or Not Reported`

Variables:
- `BLIND_SPOT_DETECTION`  
- `LANE_DEPARTURE_WARNING`  
- `AUTO_CRASH_NOTIFICATION`  
- `FRNT_COLLISION_WARNING`  
- `CRASH_IMMINENT_BRAKE`  
- `DYNAMIC_BRAKE_SUPPORT`  
- `ARS` – Automatic Rollover System  
- `NHTSA_ESC` – Electronic Stability Control  
- `SAFETY_COUNT` – Number of safety technologies present in the vehicle.

## Notes

- Multiple rows may have the same `SERIAL_CRASH` if multiple vehicles were involved in a single incident.  
- Some rows contain vehicles with no driver present, indicated clearly in `IS_DRIVER_PRESENT` and related fields.  
- Pre-crash events columns (`P_CRASH1NAME` to `PCRASH5NAME`) describe the dynamic sequence leading up to the crash.
- `SAFETY_COUNT` allows summarizing the total active safety systems per vehicle.

## Potential Uses

- Analysis of crash risk factors by speed, road conditions, or driver behavior.  
- Evaluation of advanced safety systems’ effectiveness.  
- Identification of patterns in high-severity crashes.  
- Data-driven traffic safety policy recommendations.