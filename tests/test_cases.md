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
