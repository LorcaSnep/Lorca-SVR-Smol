To begin, this project is in progress and is in no way ready for full deployment.

## Overview
I began this project with the goal of designing a very compact FBT tracker based on the Nordic Semiconductor NRF52840 utilized in the Smol SlimeVR Project.  To limit the immediate complexity of the design, I opted to utilize the Insight ISP1807.  This part combines the NRF52840 with an antenna and all of the associated components along with a number of other required components.  This makes it a very easy way to simply "drop" an NRF52840 into a design.  In addition to the ISP1807, this design utilizes an LSM6DSVTR IMU and a QMC6309 magnetometer.

One aspect of this tracker that is a significant departure from similar designs is the charging dock.  I personally do not like using USB-C as a docking connector.  With how compact I am aiming for this design to be, there is no room for a second connector.  As such I have elected to only have a docking connector based on pogo pins.  This design has also allowed me to design the 3.3V regulator in a way that it starts up when the tracker is removed from the dock.

## Project Status

As of 3/3/26, I am awaiting delivery of the first PCBs and components and I have not begun testing the case components.  The next step is to test the PCBs when they arrive and determine if any changes need to be made before I begin refining the case hardware.  Additionally, I have not started working on the dock yet.  I have designed a temporary programming one but the final one has not been designed.

## Current PCB Design

![Error](https://github.com/LorcaSnep/Lorca-SVR-Smol/blob/main/Images/Lorca%20SVR%20Smol%20PCB%20Front.PNG)

![Error](https://github.com/LorcaSnep/Lorca-SVR-Smol/blob/main/Images/Lorca%20SVR%20Smol%20PCB%20Back.PNG)
