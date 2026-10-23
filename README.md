# Bankai: Quadcopter Build and Flight

A quadcopter assembled from individual components and flight-tested during a robotics engineering internship at **Setscentral Ltd.**, Jimeta-Yola, Adamawa State, Nigeria (September to November 2022).

![Bankai quadcopter](images/bankai_quadcopter.jpg)

Over roughly four weeks of testing (four sessions a week, at least three hours per session), the team took turns piloting Bankai in flights of ten-plus minutes each, eventually achieving stable controlled flight at altitudes exceeding a two-storey building. The flight controller was fully calibrated within four attempts, helped by earlier simulated flight training in RealFlight.

## Overview

The goal was to understand how the major subsystems of a quadcopter work together to produce controlled, stable flight. The project went from learning basic drone flight in a desktop simulator, to assembling and calibrating the physical aircraft, to flying it.

It gave practical experience in UAV components, mechanical assembly, electronic integration, flight-controller configuration, calibration, battery management, simulation, and flight testing.

![Bankai with the team](images/bankai_with_team.jpg)

## Simulation

Before flying the real aircraft, I used the **RealFlight** drone simulator to practise basic flight and transmitter control on obstacle courses. This was a low-risk way to build an initial feel for quadcopter flight dynamics before physical testing.

## System Design

Bankai has four main subsystems:

| Subsystem | Contents |
|---|---|
| Propulsion | Motors, propellers, electronic speed controllers (ESCs) |
| Flight control | Flight controller and onboard sensors |
| Auxiliary | GPS and compass |
| Payload | Components added for the drone's intended application *(add details if applicable)* |

## Components

| Component | Specification |
|---|---|
| Frame | HolyBro S500 480 mm quadcopter frame |
| Motors | 2212 920KV brushless motors (CW/CCW) |
| Propellers | 1045 propellers |
| ESCs | 30A 3-4S ESC x4 |
| Flight controller | Pixhawk 2.4.8 32-bit |
| Radio system | FLYSKY transmitter with IA6B receiver |
| Battery | LiPo 5200 mAh, 11.1 V (3S), 60C, XT60 connector |
| GPS | M8N GPS module with compass |
| Charger | B6 V3 Smart Charger |
| Ground control software | Mission Planner |
| Flight simulator | RealFlight |

![Frame arms and landing gear](images/frame_arms_and_landing_gear.jpg)
![HolyBro S500 frame plate](images/holybro_s500_frame_plate.jpg)
![M8N GPS module and brushless motors](images/m8n_gps_and_motors.jpg)

## Build and Integration

**Mechanical assembly.** The HolyBro S500 frame and arms were joined with fasteners. The four brushless motors were bolted to the arms, with attention to clockwise and counter-clockwise orientation, which matters for yaw stability.

**Electrical integration.** Each ESC was connected to its motor. The ESC leads were soldered to the power distribution board with positive and negative connections matched, and continuity tests were done before powering the system.

**Flight controller integration.** The Pixhawk was connected to:

- ESC motor channels
- FLYSKY IA6B receiver
- M8N GPS and compass
- Power module (which also monitors battery voltage and current)
- Safety switch

## Calibration

Calibration was done in **Mission Planner** and covered:

- Accelerometer calibration
- Compass calibration
- Radio transmitter calibration
- Channel mapping and endpoint verification
- Motor direction verification
- ESC calibration

Several attempts were needed before all sensors calibrated successfully.

## Battery Management and Safety

- The 3S LiPo was charged with a B6 V3 Smart Charger, with the cells balanced before use.
- Propeller tightness was checked before every flight to reduce the risk of mechanical failure.

## Flight Testing

After assembly and calibration, Bankai flew successfully. Testing ran for about four weeks, with the team taking turns as pilot, and reached stable controlled flight above the height of a two-storey building.

| Item | Result |
|---|---|
| Test period | ~4 weeks, 4 sessions/week, 3+ hours/session |
| Flight duration | 10+ minutes per flight |
| Maximum altitude | Above a two-storey building *(add measured value if available)* |
| Calibration | Completed within 4 attempts |

![Bankai on the ground](images/bankai_on_ground.jpg)

## Challenges and Solutions

| Challenge | How it was resolved |
|---|---|
| Understanding CW/CCW motor arrangement and its effect on yaw stability | Studied quadcopter propulsion principles and reviewed the HolyBro S500 documentation |
| Clean ESC-to-power-board soldering | Careful soldering, with continuity testing after each connection |
| Mission Planner calibration needed exact procedures and correct physical orientation of the aircraft | Repeated the sequence until it completed |

## What I Learned

- How the individual UAV components work and interact as a system
- Assembling a quadcopter from separate parts
- Soldering, continuity testing, and hardware troubleshooting
- Configuring and calibrating a Pixhawk with Mission Planner
- Setting up a radio transmitter and receiver
- Charging and handling a three-cell LiPo
- Using simulation to build piloting skills, then flying the real aircraft
- Basic pre-flight safety procedures

## What I Would Do Differently

- Add a current sensor from the start for more detailed power monitoring
- Use vibration damping for the flight controller to reduce IMU noise
- Calibrate each ESC individually before connecting the whole system

## Project Context

- **Organisation:** Setscentral Ltd.
- **Location:** Karewa, Jimeta-Yola, Adamawa State, Nigeria
- **Internship:** Robotics Engineering Internship
- **Period:** September to November 2022
- **Team project:** built and flown by a team; *(add a line on your specific contribution)*

## Repository Contents

```
bankai-quadcopter/
├── README.md
├── images/
└── references/
    └── component_datasheets.md
```

## Author

Toluwanimi Williams Olatokun
B.Eng. Mechatronics Engineering
Contact: olatokuntoluwanimi@gmail.com
