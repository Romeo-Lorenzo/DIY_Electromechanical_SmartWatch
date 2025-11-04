# DIY Quartz Watch project

## Introduction
This is my take at making my own quartz watch with a twist.
Driven by a PCF2003 chip from NXP as well as an STM32WB for bluetooth capability and controlling the subdial driving system in order to display data from the equipped sensors:
- Barometer
- Compass
- VBat
- Temp
- 1 cell lithium charge and discharge
- Very low power circuitry, 150nA continuous current consumption and 150mA with STM32 turned on. Designed to be equipped of two Airpods1 batteries in parralel for 50mAh total.

## Hardware:

  The hardware is divided into electrical and mecanical hardware

  ### Electrical:
  - 6 layer 36mm PCB board designed to replace original PCB from a Miyota 2035 movement. The PCB has two contact pads for two Miyota 2035 movements to drive both main and sub-dial. It is equipped with contact pads to ease programming of both the STM32 and the PCF 2003, most likely with pogo pin alignement 3D print to come.

<img width="400" height="215" alt="PCB dial side" src="https://github.com/user-attachments/assets/4ed879fc-20d3-4d53-8b59-69d74cefa0cb" />
<img width="400" height="208" alt="PCB caseback side" src="https://github.com/user-attachments/assets/e4aaae91-5e44-46f8-8ce4-9df213fd7eaf" />
<img width="400" height="203" alt="PCB" src="https://github.com/user-attachments/assets/56441785-9042-4be3-a35e-da0c90de2531" />
  
  - TODO Monolayer PCB to mount as shield on Nucleo board equipped with OP Amp to be able to output the voltage necessary to program the PCF 2003. Will most likely be designed as a programming station and include the pogo pins and debug connector for programming the STM32 as well and be integrated with the forementioned 3d model to print.
 
  ### Mecanical:
  - Onshape designed 36mm watch case with high water resistance in mind, a water tight push button to control subdial and STM32 ON time.
<img width="300" height="300" alt="36mm Watch" src="https://github.com/user-attachments/assets/9d7af323-d3b8-4e70-af7a-c2b6f5cbc723" />
<img width="300" height="300" alt="36mm Watch Front" src="https://github.com/user-attachments/assets/97586367-8ad1-4e33-b455-0be09d7bcf9f" />
<img width="300" height="300" alt="36mm Watch pcb angle rear" src="https://github.com/user-attachments/assets/f89747ea-07de-45ba-bea7-bdac2633e431" />
<img width="300" height="300" alt="36mm Watch Fornt mounted" src="https://github.com/user-attachments/assets/9fd1f594-4f48-4b3b-88ed-fbcb0ad3bd4a" />
<img width="420" height="300" alt="36mm Watch rear side mounted" src="https://github.com/user-attachments/assets/524306a9-8464-4572-9ad1-8b69763388f2" />

Note that the Miyota 2035 movements will have to be modified, taking it apart and filing away the excess material on the bottom holding plate for the subdial movement is an easy fit and a tutorial on how to take apart and prepare the movements will be released.
The case is not yet finished but I estimate a 5 atm water tight watch, tolerances for CNC machinig will have to be tested. Crown will be a screw-in watertight type, a silicon membrane will ensure watertightness of the push button all the while allowing the inside barometer to read pressure, especially fun underwater.
