# System Architecture


## Overview

The system is a low-cost robotic actuator testbed designed for wearable robotics research.


## System Flow


Desired Torque Command

↓

STM32 Controller

↓

Motor Driver

↓

DC Geared Motor

↓

Mechanical Joint

↓

Sensors

- Encoder
- Current Sensor
- Load Cell


↓

Torque Estimation Algorithm

↓

Feedback Controller

↓

Motor Adjustment



## Hardware Components


### Controller

STM32F411 BlackPill

Function:
- Sensor acquisition.
- Control algorithm execution.
- Motor command generation.


### Actuator

12V DC Geared Motor

Function:
- Generate mechanical torque.


### Motor Driver

BTS7960

Function:
- Provide power control.
- Control motor direction and speed.


### Sensors

Encoder:
- Joint position measurement.

Current Sensor:
- Motor current measurement.

Load Cell:
- Reference torque measurement.


## Control Architecture


Input:

Desired torque


Controller:

Torque estimation + PID + impedance controller


Output:

Motor torque


Feedback:

Estimated torque compared with target torque.


## Research Focus

The main research focus is:

Low-cost actuator torque estimation and control for wearable robotics applications.
