# Tyro69 Guide

The following is a guide on the Tyro69; its components, how to build it, the transmitter (the remote control) and charging the batteries.
Where possible I've added general advice which can be applied to any drone.
This was my first introduction to the world of drones and where there was a mistake to be made, I probably made it. I found that there is a wealth of information out there but when you're completely new to any kind of electronics it's really difficult to find relevant information all in one place and it's so easy to miss the subtlties. However, I've persevered and this is a compilation of what I've learned.


### Components

##### ESC
Eachine 20A BLHeli_S 4in1 ESC

ESC comes with a 25V 150uF capacitor to be soldered on


##### Flight Controller
Eachine F411 OSD Flight Controller

##### Motors
Eachine 1104 8600KV 2-3S Motor x4
What does each part of the name mean?
1104 is the motor size. It means that the stator width is 11mm and the stator height is 4mm.
8600KV means the RPM (rotation per minute) is 8600 for every volt. I use a 3s battery (11.1V) so the motors spin at (8600 x 11.1) 95460 RPM without props on.
2-3S means that a 2S or 3S LiPo battery is appropriate

##### Propellers
2mm props

##### Receiver
Frsky XM+ Micro D16 SBUS Full Range Mini RC Receiver
Must make sure you get the receiver that matches the brand of your transmitter.
The SBUS part here is important and leads to adjustments you have to make to the flight controller.

##### 18AWG XT30 pigtail
Note this is the female

### The Build
The first step was to solder on the motors. Each motor has three wires. Tin each of the twelve pads (3x4) with a small amount of solder. Trim back the wire casing and solder each wire down onto the pad. Here I came to my first mistake. The tutorial I watched just said to match up the wires to three adjacent pads in whatever combination. In didn't mention that the order in which you place them affects the direction that the motors spin. We need opposite motors to spin the same direction. I have it so that 
So you need to cross two of the wires for anticlockwise rotation.





### FrSky Transmitter



### Charging
Quick Intro: Most drones/quadcopters/RC stuff use LiPo batteries. There are loads of videos showing you how to take proper care of these batteries as when used inappropraitely have been known to catch fire. These batteries come in different voltages i.e. cell counts. 2s = 2 cells. Voltage is directly proportional to the power generated by the motors so higher voltage means motors to produce more power, but they also add more weight.
I use a 3S LiPo battery which has a XT30 female connection. I use iMax B6 charger which balance charges the multiple cells of the battery. A quick problem I ran into was the lack of adapter and surrounding advice on how to charge this battery. Essentially the iMax B6 has a Deans T plug connection so it needs an XT30 male to Deans T plug female adapter.
