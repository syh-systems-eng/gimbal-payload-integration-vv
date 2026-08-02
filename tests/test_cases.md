# Integration Test Cases
This document defines initial integration test cases for the EO/IR Gimbal Playload Integration System.

## GP-TC-001 - Verify slew/pan/tilt command execution
| Field | Details |
|---|---|
| Requirement(s) | GP-REQ-001 |
| Objective | Verify that movement commands from the mission system are received and executed by the gimbal playload. |
| Preconditions | Gimbal playload is powered on and connected to the mission system. || Input | Operator sends slew, pan, and tilt commands. |
| Input | Operator sends slew, pan, and tilt commands. |
| Exepected Result | Gimbal moves to the commanded posisition and reports updated position status. |
|Integration Point | Mission system → Gimbal payload |
| Status | Not Run | 

## GP-TC-002 - Verify zoom command execution
| Field | Details |
|---|---|
| Requirement(s) | GP-REQ-003 |
| Objective | Verify that zoom commands from the mission system are received and executed by the gimbal camera. |
| Preconditions | Gimbal camera is active and video output is available. |
| Input | Operator sends zoom-in and zoom-out commands. |
| Expected Result | Camera zoom level changes according to command and updated zoom status is reported. |
| Integration Point | Mission system → Gimbal camera |
| Status | Not Run |

## GP-TC-003 - Verify EO/IR sensor mode switching
| Field | Details |
|---|---|
| Requirement(s) | GP-REQ-005 |
| Objective | Verify that the system can switch between EO and IR sensor modes. |
| Preconditions | EO and IR channels are available. |
| Input | Operator switched sensor mode from EO to IR, then IR to EO. |
| Expected Result | Correct sensor mode becomes active and video output corresponds to selected mode. |
| Integration Point | Aircraft motion data → Gimbal stabilisation → Video output |
| Status | Not Run |

## GP-TC-005 - Verify target tracking feedback
| Field | Details |
|---|---|
| Requirement(s) | GP-REQ-007 |
| Objective | Verify that tracking status is reported to the mission system during target tracking. |
| Preconditions | Target tracking mode is active. |
| Input | Operator selects a target for tracking. |
| Expected Result | System reports tracking active status and displays tracking feedback on the mission display. |
| Integration Point | Gimbal payload → Mission system display |
| Status | Not Run |

## GP-TC-006 - Verify movement command failure warning
| Field | Details |
|---|---|
| Requirement(s) | GP-REQ-002 |
| Objective | Verify that the system generates a warning indication when movement commands are not successfully executed by the gimbal payload. |
| Preconditions | Mission system and gimbal payload are powered on and connected. |
| Input | Operator sends a slew, pan, or tilt command. Simulate a communication failure or command execution failure within the gimbal payload. |
| Expected Result | A warning indication is displayed to the pilot or mission operator. Fault status is reported to the mission system. |
| Integration Point | Mission system → Gimbal payload → Mission system display |
| Status | Not Run |

## GP-TC-007 - Verify zoom command failure warning
| Field | Details |
|---|---|
| Requirement(s) | GP-REQ-004 |
| Objective | Verify that the system generates a warning indication when zoom control commands are not successfully executed by the gimbal payload. |
| Preconditions | Mission system and gimbal payload are powered on and connected. |
| Input | Operator sends zoom-in and zoom-out commands. Simulate a camera malfunction or zoom command execution failure within the gimbal payload. |
| Expected Result | A warning indication is displayed to the pilot or mission operator. Fault status is reported to the mission system. |
| Integration Point | Mission system → Gimbal payload → Mission system display |
| Status | Not Run |

## GP-TC-008 — Verify tracking loss warning
| Field | Details |
|---|---|
| Requirement(s) | GP-REQ-008 |
| Objective | Verify that the system generates a warning indication when tracking feedback is interrupted or lost. |
| Preconditions | Mission system and gimbal payload are powered on and connected. Target tracking mode is active. |
| Input | Operator initiates target tracking. Simulate loss of tracking data or tracking failure within the gimbal payload. |
| Expected Result | A warning indication is displayed to the pilot or mission operator. Fault status is reported to the mission system. |
| Integration Point | Mission system → Gimbal payload → Mission system display |
| Status | Not Run |

## GP-TC-009 — Verify Low Power Warning
| Field | Details |
|---|---|
| Requirement(s) | GP-REQ-009 |
| Objective | Verify that the system generates a low-power warning when the available power falls below 30% of nominal operating capacity and clears the warning when power is restored above the threshold. |
| Preconditions | Mission system and gimbal payload are powered on and operating normally. Available power is greater than 30%. |
| Input | Simulate the available power decreasing from 30% to 29%, then increasing back above 30% after recharge. |
| Expected Result | A low-power warning is displayed when the available power falls below 30%. The warning remains active while the power level is below 30% and clears automatically once the power level is restored above the defined threshold. |
| Integration Point | Power management subsystem → Gimbal payload → Mission system display |
| Status | Not Run |

## GP-TC-010 — Verify environmental robustness during adverse weather
| Field | Details |
|---|---|
| Requirement(s) | GP-REQ-009 |
| Objective | Verify that the gimbal payload maintains operational functionality, image stabilisation, and system status reporting during simulated adverse environmental conditions. |
| Preconditions | Mission system and gimbal payload are powered on and operating normally. Environmental simulation is available. One environmental condition is introduced per test run. |
| Input | Simulate adverse environmental conditions such as turbulence, heavy rain, strong wind gusts, or thunderstorms. After completing individual scenarios, execute combined environmental conditions (e.g. turbulence + heavy rain, turbulence + strong wind gusts). Vary disturbance severity from low to medium to high. |
| Expected Result | The gimbal payload continues to provide stabilised imagery, tracking feedback, and system health status. If operational limits are exceeded, the system shall generate an appropriate warning or transition to a degraded operating mode. |
| Integration Point | Environmental simulation → Aircraft motion/environment → Gimbal payload → Mission system display |
| Status | Not Run |
