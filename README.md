# Project Sense

Team Members:
- Jerome Dinakar (jeromed2)
- Abhay Narayanan (abhayn2)
- Aakash Rangan (arangan3)

# Problem

There are many cases where it is perilous for cyclists on anything from rapid highways to busy inner city roads. This is further exacerbated in a variety of situations that may cause drivers to fail to notice cyclists before an accident may happen. For example, unfavorable weather conditions could cause poor visibility, or there may even be blind corners in congested urban centers. Naturally, these are both cases where a camera, which appears to be the obvious solution, is rather ineffective in warning a vehicle driver that there are cyclists ahead. 

On the other side of the coin, cyclists are also frequently unaware that vehicles may be approaching. Once more, simple side-mirrors or anything of the sort are impractical due to the aforementioned reasons. 

Therefore, there appears to be a space for a product to fill, such that both the drivers and cyclists are suitably warned to avert collisions. 


# Solution

In order to solve the previous problem, it seems pertinent to take a two-pronged approach. 

The first is to notify the driver with a sound within the vehicle when a cyclist (using transmitters and receivers) is found within range. This alerts the driver to observe a display (obtains information from the microcontroller) that depicts the approximate position of any cyclists in the immediate vicinity in relation to the vehicle. In this manner, the driver can proceed with caution, and can even be aware of cyclists that are not yet visible.

The second half is to notify the cyclist that a vehicle is approaching, along with a reading of the distance said vehicle is from that point (using a microcontroller). This would not only be useful for what was previously mentioned, but also to notify the cyclist that a vehicle may be approaching from behind. This may go unnoticed even in ideal visibility conditions. 

Both halves serve to afford the personnel a modicum of warning, allowing them to take appropriate precautions. Both aspects of the product have the potential to save lives.


# Solution Components

Bike PCB

## Subsystem 1: Transmitter

For every Bike PCB/device we will assign a unique device ID. The Transmitter of the Bike PCB will transmit the unique Bike Device ID radially outwards. 
(Digi-key Part No. : 1597-114992732-ND) RF Transmitter and Receiver

## Subsystem 2: Receiver

The Bike PCB will also require a Receiver that detects the confirmation and associated timestamp from any nearby Car Devices. 
(Digi-key Part No. : 1597-114992732-ND) RF Transmitter and Receiver

## Subsystem 3: Battery Subsystem
A standard 9V battery along with voltage regulators will allow us to power the Transmitter, Receiver, Microcontroller, and LEDs in our design.
(Digi-key Part No. : S-19214B00A-V5T2U7) Voltage Regulator

## Subsystem 4: Microcontroller
Our Microcontroller will handle basic computations such as calculating the distance between the vehicle and biker, and selecting which LED to raise to notify the biker the approximate distance of the nearest vehicle.
(elegoo atmega328p: https://www.amazon.com/ELEGOO-Arduino-ATmega328P-Without-Compatible/dp/B0713XK923?th=1)

Car PCB

## Subsystem 1: Transmitter

The Transmitter of the Car PCB will transmit a confirmation the Bike ID was received, Car ID ,and a timestamp for when the signal was transmitted.
(Digi-key Part No. : 1597-114992732-ND) RF Transmitter and Receiver

## Subsystem 2: Receiver

The Car PCB will also require a Receiver that receives the Bike ID
(Digi-key Part No. : 1597-114992732-ND) RF Transmitter and Receiver

## Subsystem 3: Battery Subsystem
A standard 9V battery along with voltage regulators will allow us to power the Transmitter, Receiver, Microcontroller, and Display in our design
(Digi-key Part No. : S-19214B00A-V5T2U7) Voltage Regulator

## Subsystem 4: Microcontroller
Our Microcontroller will store unique Bike IDs to distinguish bikes between one another. The microcontroller will also record angle of incidence to send to the Display.
(elegoo atmega328p: https://www.amazon.com/ELEGOO-Arduino-ATmega328P-Without-Compatible/dp/B0713XK923?th=1)

## Subsystem 5: Display
We will use a display that approximately shows the biker’s relative location to the driver.
(Digi-key Part No: 2632-E144RB-FW400-R-ND) LCD Display



Our goal is to create a system that can successfully detect and communicate awareness between the bicycle and vehicle. We aim to test this reliability in signal detection and communication from at least 10 meters to 40 meters away between the two devices, accurately sending and picking up RF signals at speeds of 10 miles per hour. The devices will also be able to inform both the biker and driver about their relative locations to each other.

