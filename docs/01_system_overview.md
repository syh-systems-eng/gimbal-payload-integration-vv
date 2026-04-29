## System Under Test

The System Under Test is an EO/IR gimbal payload integrated with an aircraft or UAV mission system, responsible for stabilised imaging, target tracking, and situational awareness.

The system is evaluated not only for individual component functionality but also for its ability to operate as part of an integrated system under various operational and environmental conditions.

## Inputs

- Gimbal movement commands (slew, pan, tilt) issued by the operator or mission system
- Camera zoom commands controlling optical magnification levels
- Sensor mode selection (Electro-Optical / Infrared)
- Aircraft motion data (e.g. movement, orientation) affecting stabilisation
- Power state information and battery level status
- Tracking commands for single or multiple targets

## Outputs

- Video stream output (EO/IR) to the mission system display
- Gimbal position data (azimuth and elevation angles)
- Target tracking status and tracking feedback
- System health status for operator awareness
- Warning flags for faults (e.g. movement limitation, low power, tracking loss)
- Target location data (e.g. coordinates relative to observed terrain)
