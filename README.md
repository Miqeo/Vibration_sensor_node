# Vibration sensor node

![](/images/casing_transparent.png)

## Motivation

Since my first endeavour into PCB and CAD design, I have always wanted to create something from start to finish. This was possible with one of the previous projects I was a part of, where there was a need to make a Raspberry Pi HAT, the software to run with it, and the corresponding casing.

As that project came to a close, I wanted to make use of my time and extend my knowledge with this initiative to make something useful and to test the capabilities of FOSS software such as Freecad and Kicad.

This culminated in the amalgamation of sensors, storage, comms, and compute that can be called a “node” for the distributed sensor system.

As this is a work in progress, and the exact use might change with time, I do not want to point towards the problem it might, in the future, solve. The time-synchronised system of this kind may be used in places where other, physically connected or remote nodes are used now.

## Future capabilities

The planned capabilities of the node are to autonomously save vibration data and synchronize it with other nodes using a wireless link.

## System elements

The system makes use of the small cyllindrical battery, repurposed from an ellectrical cigarette. The main computation is done by the STM32 microcontroller, which has access to the onboard accrellerometer-gyroscope combo and an extensible accelerometer via a board-to-board connector. The microcontroller is connected to the outside world via the wireless module and usb 2.0 via USB-C, which also acts as the charger for the unit. The data collected can be stored on the external SD card or the soldered-on QSPI flash.

[Here is the schematic document of the controller board](/pcb/accel_controller_schematic.pdf)


![](/images/accel_data_diagram.png)

*Data flow of the system*

## Fabrication

![](/images/controler_pcb.png)

*The main controller PCB*

![](/images/subboard_pcb.png)

*A sensor sub-board connected via a board-to-board connector*

![](/images/casing_drawing_Page__.svg)

*Outside view of the sensor casing*