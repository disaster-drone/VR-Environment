# *State Farm Disaster Drone VR Environment*

### Table of Contents
1. [Description](#Description)
2. [Demo](#Demo)
3. [Installation](#Installation-Proccess) 
4. [Hardware & System Requirements](#Product-Specs)
5. [Migration Notes](#Migration-Notes)
6. [Controls](#Controls)


## Description
The VR Environment is a component of our disaster drone sysytem, serving as the fundamental environment for movement and claim creation within VR. This project was developed using Unreal Engine, utilizing the VR Template Project created by Epic Games as a starting point. Within the environment, the user can teleport virtically & horizontally, snap turn, and create claims by placing down a cone. Upon placement of a cone, the closest image captured by the drone is displayed. 



## Demo
(put video here)

## Installation



## Hardware & System Requirements
The System should function correctly with:
* Oculus Mobile: Quest 1 and Quest 2
* Oculus PC: Rift S and Quest with Oculus Link. 

However, it was only tested with the Oculus Quest 2 and the Oculus Rift. We recommend the Oculus Quest 2. https://www.meta.com/quest/products/quest-2/


**Recommended Hardware and System Requirements for the Oculus Rift:**
* Processor: Intel i5-4590/AMD Ryzen 5 1500X or greater
* Graphics Card: NVIDIA GTX 1060/AMD Radeon RX 480 or greater
* Alternative Graphics Card: NVIDIA GTX 970/AMD Radeon R9 290 or greater
* Memory: 16 GB RAM
* Operating System: Windows 10
* USB Ports: 1 x USB 3.0 port (3x USB for Oculus Rift C1)
* Video Output: Compatible DisplayPort


**Recommended Hardware and System Requirements for the Oculus Quest 2:**
* Processor: Intel i5-4590 / AMD Ryzen 5 1500X or better
* GPU: NVIDIA GeForce GTX 1070 or AMD 500 Series and higher
* Memory: 8GB
* Operating System: Microsoft Windows 10
* USB Ports: 1x USB port
* Note: The Oculus Quest is a tetherless device but you may choose to purchase Oculus Link cable to connect the Oculus Quest with your PC due to frequent connection timeouts.

System requirement information gathered from: https://circuitstream.com/blog/vr-hardware
## Migration Notes
* A tethered headset is always recommended to avoid connection timeouts.
* All blueprinting was done on SimpleUI and VR Pawn.
* We used the VR Template Project as a starting point. On the VR Pawn Blueprint Event Graph, everthing highlighted in dark gray was taken from the VR Template Project and everything highlighted in white is our work.
* 

## Controls
