To begin, this project is in progress and is in no way ready for full deployment.

## Overview
I began this project with the goal of designing a very compact full body tracker based on the Nordic Semiconductor NRF52833 utilized in the Smol SlimeVR Project.  To limit the immediate complexity of the design, I opted to utilize the Insight ISP1907-HT.  This part packages the NRF52833 with an antenna and all of the associated components along with a number of other required components.  This makes it a very easy way to simply "drop" an NRF52833 into a design.  In addition to the ISP1907-HT, this design utilizes an IMU (either an ICM-45686 or LSM6DSVTR) and a QMC6309 magnetometer.

One aspect of this tracker that is a significant departure from similar designs is the charging dock.  I personally do not like using USB-C as a docking connector.  Since is is possible for the connector to move relative to the body of the device, even just a small amount, it can be a little clunky.  If I were to add a second connector for a dedicated dock connection, this would dramatically increase the space required on the PCB for both connectors.  As such, I have elected to only have a docking connector based on pogo pins.  The tracker has a secondary PCB mounted perpendicular to the primary one which provides the landing pads for the pogo pins in the charging dock.  This design has also allowed me to design the 3.3V regulator such that it starts up when the tracker is removed from the dock.

The case hardware for the trackers is primarily 3D printed.  There are two halves to this tracker connected by a flexible bridge in the middle.  One side contains the battery, and the other side contains the PCB.  The solid cases are printed out of PLA and the flexible bridge is cast out of silicone.

In addition to the trackers, I have designed a charging dock / base station for the trackers.  There are three subsystems in this dock: charging, programming, and the receiver.  The charging system consists of ten charging bays for the trackers, along with a TPS259631 efuse, STUSB4500L USB-C port controller, ATTINY3217 microcontroller and all of the required components for these components.  These allow the dock to regulate and control the power.  The programming system consists of one additional bay reconfigured so the tracker can be powered on in the bay and connected via usb to a computer for firmware flashing.  The final system is the receiver.  For now this is just a pass through from the USB-C port to a vertical USB-A port for the receiver to plug into the dock.  In a future revision I would like to integrate the receiver into the design of the dock.  Like the trackers, the case components for the charging dock are 3D printed out of PLA.

## Project Status

As of 10/21/26, I am awaiting delivery of the first PCBs and components and I have begun printing case prototypes.  

## Current Tracker PCB Design

# ICM-45686

![Error](https://github.com/LorcaSnep/Lorca-SVR-Smol/blob/main/Images/SVR%20Lorca%20PCB%20Front.PNG)

![Error](https://github.com/LorcaSnep/Lorca-SVR-Smol/blob/main/Images/SVR%20Lorca%20PCB%20Back.PNG)

# LSM6DSVTR

![Error](https://github.com/LorcaSnep/Lorca-SVR-Smol/blob/main/Images/SVR%20Lorca%20PCB%20Front.PNG)

![Error](https://github.com/LorcaSnep/Lorca-SVR-Smol/blob/main/Images/SVR%20Lorca%20PCB%20Back.PNG)

# Charging Dock

![Error](https://github.com/LorcaSnep/Lorca-SVR-Smol/blob/main/Images/SVR%20Lorca%20PCB%20Front.PNG)

![Error](https://github.com/LorcaSnep/Lorca-SVR-Smol/blob/main/Images/SVR%20Lorca%20PCB%20Back.PNG)
