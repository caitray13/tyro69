# Tyro69 Guide

The following is a guide on the Tyro69; its components, how to build it, the transmitter (the remote control) and charging the batteries.
Where possible I've added general advice which can be applied to any drone.  
This was my first introduction to the world of drones and where there was a mistake to be made, I probably made it. I found that there is a wealth of information out there but when you're completely new to any kind of electronics it's really difficult to find relevant information all in one place and it's so easy to miss the subtlties. However, I've persevered and this is a compilation of what I've learned.  


### Components

#### ESC
Eachine 20A BLHeli_S 4in1 ESC  
ESC comes with a 25V 150uF capacitor to be soldered on


#### Flight Controller
Eachine F411 OSD Flight Controller

#### Motors
Eachine 1104 8600KV 2-3S Motor x4  
What does each part of the name mean?  
1104 is the motor size. It means that the stator width is 11mm and the stator height is 4mm.  
8600KV means the RPM (rotation per minute) is 8600 for every volt. I use a 3s battery (11.1V) so the motors spin at (8600 x 11.1) 95460 RPM without props on.  
2-3S means that a 2S or 3S LiPo battery is appropriate

#### Propellers
2mm props  

#### Receiver
Frsky XM+ Micro D16 SBUS Full Range Mini RC Receiver  
Must make sure you get the receiver that matches the brand of your transmitter.  
The SBUS part here is important and leads to adjustments you have to make to the flight controller.  

#### 18AWG XT30 pigtail
Note this is the female  

### The Build
1. Solder on the motors. 
Each motor has three wires. Tin each of the twelve pads (3x4) with a small amount of solder. Trim back the wire casing and solder each wire down onto the pad. Here I came to my first mistake. The tutorial I watched just said to match up the wires to three adjacent pads in whatever combination. It didn't mention that the order in which you place them affects the direction that the motors spin. It's true you can change this in the software later but tbh just do it now. We need opposite motors to spin the same direction.  
I have it so that 2 o clock and 8 o clock spin clockwise, whereas the other two spin anticlockwise.  
So you need to cross two of the wires for anticlockwise rotation.

![motor_rotation](https://github.com/caitray13/tyro69/blob/master/images/motor_rotation.PNG)

Another tip is to solder them on the underneath of the ESC since it makes the drone neater. 

2. Solder on the battery lead. 
Mine came off quite easily in the first test run because it's heavier than the other wires so make sure you do this properly. 

3. Solder on the capacitor. 
Self explanatory, just make sure you use enough solder since it's heavier. Also try to not keep the soldering iron on the capacitor for too long, it's quite conductive. 

4. Screw the motors.  
Make sure you screw in each motor **tight**. The motors spin very past and the screws can wiggle loose a bit too easily otherwise. Here you can use electrical tape to stick the wires to the frame or bend them under the ESC - either way, make sure they're out of the way of the props.  

5. Solder on the receiver.  
I have a FrSky transmitter so I needed a FrSky receiver. SBUS is a popular receiver (RX) protocol. It is a digital signal so it's faster than older ananlogue signals such as PPM. An adjustment needs to be made to the fligh controller and that is to bridge two solder pads together next to where the reciever is plugged in. This tells the Tyro that you're using SBUS.  
Now you needs to solder the three wires (yellow, red and black) from the receiver cable onto the receiver. Then plug in the cable to the flight controller.  
You don't need to know this but in case you're interested:  
 - black wire = GND (protective conductor to prevent shock/fire, also called Earth wire)
 - yellow wire = signal (S.Bus)
 - red wire = power 
 
 6. Frame Assembly.  
 First, attach the battery strap.  
 Second, four long bolts, rubber guards.  
 Third, ESC and more rubber guards.  
 Fourth, receiver.  
 Fifth, flight controller and bolts.  

### Betaflight  
Betaflight was the challenge I wasn't expecting. It's flight controlling software. To use it you needs to download several drivers. Best thing to do is watch this video: 
https://www.youtube.com/watch?v=xmaTq4JgTXI&list=PLugTF0N_ig3z6zBsPWqZFJq6JhpAFmS9H&index=2&t=1869s  
The video covers the drivers, flashing the flight controller to latest version of Betaflight (MATEKF411), binding the recevier (I have more on that), channel mapping, arming, etc.
** It's so tempting but DO NOT skip the arming step. It's a failsafe that I've needed several times. **


### FrSky Transmitter
Binding the receiver to the transmitter is pretty painless. There's loads more you can do with the transmitter but for basics just follow this https://www.youtube.com/watch?v=ZOBwwNpjNrY&list=PLugTF0N_ig3z6zBsPWqZFJq6JhpAFmS9H&index=3&t=0s  


### Charging
Quick Intro: Most drones/quadcopters/RC stuff use LiPo batteries. There are loads of videos showing you how to take proper care of these batteries as when used inappropriately have been known to catch fire. These batteries come in different voltages i.e. cell counts. 2s = 2 cells. Voltage is directly proportional to the power generated by the motors so higher voltage means motors to produce more power, but they also add more weight.  
I use a 3S LiPo battery which has a XT30 female connection. I use iMax B6 charger which balance charges the multiple cells of the battery. A quick problem I ran into was the lack of adapter and surrounding advice on how to charge this battery. Essentially the iMax B6 has a Deans T plug connection so it needs an XT30 male to Deans T plug female adapter.
