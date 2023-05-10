# *State Farm Disaster Drone VR Environment*

### Table of Contents
1. [Description](#Description)
2. [Demo](#Demo)
3. [Installation](#Installation-Proccess) 
4. [Hardware & System Requirements](#Product-Specs)
5. [Migration Notes](#Migration-Notes)
6. [Controls](#Controls)


## Description
The VR Environment is a component of our disaster drone sysytem, serving as the fundamental environment for movement and claim creation within VR. This project was developed using Unreal Engine, utilizing the VR Template Project created by Epic Games as a starting point. Within the environment the user can teleport vertically & horizontally, snap turn, and create claims by placing down a cone. Upon placement of a cone, the closest image captured by the drone is displayed. 


## Demo
**Full Demo Video:** https://youtu.be/faXq7GY65Ww

## Installation
**Prerequisites**
Download Unreal Engine Editor Version: 5.0.3-20979098+++UE5+Release-5.0.

Download the Oculus App on your Desktop.

Set up your VR Headset on the Oculus App.

Clone the repository
~~~
$ git clone https://github.com/disaster-drone/VR-Environment.git
~~~
Launch the Unreal Engine Project File called    ![image](https://github.com/disaster-drone/VR-Environment/assets/94029910/ab4b8608-72cc-42fd-bd23-de033497288c)    to edit the project


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
* Memory: 8 GB RAM
* Operating System: Microsoft Windows 10
* USB Ports: 1x USB port
* Note: The Oculus Quest is a tetherless device but you may choose to purchase Oculus Link cable to connect the Oculus Quest with your PC due to frequent connection timeouts.

System requirement information gathered from: https://circuitstream.com/blog/vr-hardware


## Migration Notes
* This project was developed using PC and Virtual Machine with the following specs:

| Machine Name | Operating System | GPU | Processor | RAM | Hard Disk |
| --- | --- | --- | --- | --- | --- |
| Google Cloud Compute Engine | Windows Server 2022 | 1 x NVIDIA T4 Virtual Workstation | n1-highcpu-32 (32 vCPU) | 28.8 GB | 250 GB SSD |
| Paperspace GPU VM | Windows Server 2022 | NVIDIA Quadro RTX4000 | Intel Xeon Silver 4215R (8 vCPU) | 30 GB | 250 GB SSD |
| Desktop PC | Windows 10 | NVIDIA GeForce RTX 2080Ti | AMD Ryzen Threadripper 3960X (24 vCPU) | 16 GB | 1 TB SSD |

   
* Currently, the VR Environment can hold a 3D model that is a max of 82 m x 82 m or 8200 uu x 8200 uu. If a larger 3D model needs to be added or if you wish to make the max capacity larger you will need to update these two items.

  ![image](https://user-images.githubusercontent.com/94029910/237011766-ef4d8a67-3645-4fd8-a814-5e11b900e77b.png) 

  Reminder: The model is automatically placed at (0,0,0) so after adjusting the size of these two items you should center them.
* A tethered headset is always recommended to avoid connection timeouts.
* All blueprinting was done on SimpleUI and VR Pawn.
* We used the VR Template Project as a starting point. On the VR Pawn Blueprint Event Graph, everything highlighted in dark gray was taken from the VR Template Project and everything highlighted in white is our work.
* The images taken from the drone and the .csv file containing must be put into directories /Game/VRTemplate/Blueprints/UI/Images and /Game/VRTemplate/Blueprints/UI/DataTable in order for the 'Create a Claim' function to work properly. Both of these are added automatically in script (IDK NAME ASK ASIM) under the automation repository. Should you choose to change these locations you will need to update (SCRIPT NAME) and the paths in both 'Get Assets by Path' Nodes that are called off of the 'Event BeginPlay' Event Node in the VR Pawn Blueprint Event Graph. ![image](https://user-images.githubusercontent.com/94029910/237002730-007b2348-00c7-43f2-9aac-ffff0a4a8efd.png)
  Additionally, you will need to make sure the new directories are cooked in project settings. 

  ![image](https://user-images.githubusercontent.com/94029910/237002895-e87b72bb-e430-4a42-ad9e-f99dea0e62d7.png)


## Controls
**Movement**
* Teleport
    * Move your right motion controllers thumbstick in the direction you want to move. The teleport visualizer will appear in the level to indicate where you will move to.
    * Release the thumbstick to teleport to the selected location.
    * <img src = "https://github.com/disaster-drone/VR-Environment/assets/94029910/71eb150e-0697-4b78-a74e-e419bf89e39a" width="300">

* Fly
    * Fly up: Press the right innter grip to teleport up.
    * <img src = "https://github.com/disaster-drone/VR-Environment/assets/94029910/9e881049-3215-44cb-a6b8-ee640c761122" width="300">
    * Fly down: Press the left inner grip to teleport down.
    * <img src = "https://github.com/disaster-drone/VR-Environment/assets/94029910/15e93d70-f960-481e-ae95-b33b7fc004c3" width="300">
* Snap Turn
    * To rotate your virtual character without moving your head, move your left motion controller's thumbstick in the direction you want to turn.
    * <img src = "https://github.com/disaster-drone/VR-Environment/assets/94029910/2fc62ac1-e419-4975-87eb-5d319089e425" width="300">


**Make a Claim**
* Place a Cone
    * Hold down your right motion controllers back trigger in the direction you want to place the cone. The place a cone visualizer appears in the level to indicate where the cone will be placed.
    * Release the trigger to place the cone in the selected location and toggle the UI that displays the closest camera angle.
    * <img src = "https://github.com/disaster-drone/VR-Environment/assets/94029910/558f944c-24dd-4b34-b7ad-01bac14f6f01" width="300">
* UI
    * After placing a cone, a UI menu will pop up attatched to your right motion controller.
    * To click buttons on the UI use the left motion controllers laser pointer to hover over the button you wish to press.
    * To press the button click the left motion controllers back trigger.
    * <img src = "https://github.com/disaster-drone/VR-Environment/assets/94029910/f6918c73-5f95-4c1b-94d1-07da666bcddd" width="300">

