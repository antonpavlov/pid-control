# pid-control
An implementation of a PID controller in C++ to maneuver the vehicle around a simulated track - Udacity's Self-Driving Car Nanodegree.

## Description ##
Originally provided by Udacity
This repository contains a PID controller that has, as an input, a cross track error (CTE) and the velocity (mph) of a simulated veicle and, as an output, an appropriate steering angle for a car stay in a track.

Initial repository can be found [here](https://github.com/udacity/CarND-PID-Control-Project).
## Requirements ##
In order to successfully build and run the program, the following requirements should be fulfilled:
* `cmake` equal or above version 3.5
* `make` equal or above version 4.1
* `gcc/g++` equal or above version 5.4
* [`uWebSocketIO`](https://github.com/uNetworking/uWebSockets) library

The contents of this repo were tested in Ubuntu Linux 18.04. It should work fine in Mac OS X once requirements are fulfilled. For Windows, please use Docker or other virtualization tools.

## Building and Running the code ##
In order to compile, please execute the following commands in a project folder:
1. `cmake ./` - do it once; in case of any machine or folder path changes, you may want to delete `CMakeChache.txt`.
3. `make`

In order to execute the program:
* `./pid`

Program opens a port 4567 and wait for a connection of the simulator described below.

## Validation ##
Once compiled and launched, the program tries establish a connection with a simulator through the 4567 port. The **Term 2 Simulator** software includes a graphical simulator for the PID Project on its fourth screen. The simulator will create a virtual track with a car that will be driven using the software provided by this repository.

The simulator can be downloaded [here](https://github.com/udacity/self-driving-car-sim/releases).

## License ##
All software included in this repository is licensed under MIT license terms. All additional programs and libraries have their owners and are distributed under their respective licenses. This repository contains Udacity's intellectual property. For any inquires on its reuse or commercialization, please contact Udacity at [www.udacity.com](https://www.udacity.com/) and users listed at the CODEOWNERS file.
