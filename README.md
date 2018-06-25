# pid-control
An implementation of a PID controller in C++ to maneuver the vehicle around a simulated track - Udacity's Self-Driving Car Nanodegree.

## Description ##
This repository contains a PID controller that has, as an input, a cross track error (CTE) of a simulated veicle and, as an output, an appropriate steering angle for a car stay in a track. The steering angle or gain is described by the following equation:

``
gain = -(Kp * cte + Ki * (i_error + cte) + Kd * (cte - prev_cte)
``

Coefficients for the proportional, integral and derivative terms were obtained by trial-and-error basis taking in account vehicle's speed. They are the following:
- Kp = 0.23
- Ki = 0.0
- Kd = 3.0

In a short description, the proportional coefficient (Kp) determines a speed of the system's response to error; the integral coefficient (Ki) acting over residual error by compensating a bias; and differential coefficient (Kd) or an "anticipatory control", dumps an oscillation and defines the best estimate for a set-state / current-state ratio.

A short video that shows effects of each PID component over a whole system, can be seen [here](https://youtu.be/CfiO3-dxoIk).

## Requirements ##
In order to successfully build and run the program, the following requirements should be fulfilled:
* `cmake` equal or above version 3.5
* `make` equal or above version 4.1
* `gcc/g++` equal or above version 5.4
* [`uWebSocketIO`](https://github.com/uNetworking/uWebSockets) library

The contents of this repo were tested in Ubuntu Linux 18.04. It should work fine in Mac OS X once requirements are fulfilled. For Windows, please use Docker or other virtualization tools.

Initial repository can be found [here](https://github.com/udacity/CarND-PID-Control-Project).

## Building and Running the code ##
In order to compile, please execute the following commands in a project folder:
1. `cmake ./` - do it once; in case of any folder changes, you may want to delete `CMakeChache.txt`.
3. `make`

In order to execute the program:
* `./pid`

Program opens a port 4567 and wait for a connection of the simulator described below.

## Validation ##
Once compiled and launched, the program tries establish a connection with a simulator through the 4567 port. The **Term 2 Simulator** software includes a graphical simulator for the PID Project on its fourth screen. The simulator will create a virtual track with a car that will be driven using the software provided by this repository.

The simulator can be downloaded [here](https://github.com/udacity/self-driving-car-sim/releases).

## License ##
All software included in this repository is licensed under MIT license terms. All additional programs and libraries have their owners and are distributed under their respective licenses. This repository contains Udacity's intellectual property. For any inquires on its reuse or commercialization, please contact Udacity at [www.udacity.com](https://www.udacity.com/) and its CODEOWNERS.
