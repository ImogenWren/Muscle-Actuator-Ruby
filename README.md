# linear-actuator-controller
Labview program for manual control of Linear Actuator. Interfaces NI USB6008 with Arduino UNO with Infineon Motor Shield for DC motor control.

## Linear Actuator

_Design of linear actuator is advantagious, as it includes safe "end stop" switches that safely cut power at extremes of travel._
_This means the position of the actuator does not need to be tracked for safety reasons._


## Motor Controls

The Arduino is programmed such that:

- Speed is controlled via Analog (0-5v) signal on A2 pin.
- Brake (Active Low) applies the brake UNLESS pulled HIGH
- Direction - Direction is set via HIGH/LOW on digital pin.

## Prerequisits for operation

- Actuator_Infineon_Controller software in Arduino Code folder programmed onto arduino Uno or similar with Infineon Motor Controller shield.
- Speed, Brake, Direction and GND Pins are connected between NI USB6008 and arduino.
- Pressure Sensor connected to NI USB6008


## LabVIEW Program
To run in Labview Development Environment, run Main.
To Run Executable - Double click on icon XXXXX

## Labview Panel & Controls
_Actuator is controlled via the Left and Right direction keys. Letting go of either keys automatically applies the brake_
- Speed controlled via Speed Knob
![image](https://user-images.githubusercontent.com/97303986/224076750-c9df68b5-1f01-4646-8ce0-debf2f2c3d64.png)
Actuator Status is displayed in `Motor Status` Traffic Light Cluster



### Labview Structure
_The labview program is written using a basic QMH paradigm.__ 
This enables quick response to user events such a keyboard inputs and front panel buttons.
![image](https://user-images.githubusercontent.com/97303986/224077007-153a398a-cb61-4f32-9b73-8443913aec48.png)



