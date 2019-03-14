# Acromegaly

Acromegaly is an open source project of the desk with automatically adjustable height. Position of the desk is controlled by Bluetooth Low Energy interface and dedicated iOS Application. 

Provided designs allows
* to build a mechanical frame of the desk, 
* to manufacture and program a controller and finally 
* to build a BLE client app. 

Total cost of components, manufacture and final polish is around 100$. 


## CAD project

[GitHub repo](https://github.com/antrov/acromegaly/tree/master/CAD)
 
Full documentation of mechanical parts of the desk: frame, rails, driver mounting and desktop. Supplied in english and polish.

Designed and created by Msc Leszek Andrzejewski.

![CAD project](https://raw.githubusercontent.com/antrov/acromegaly/master/docs/cad.jpg)

## PCB schematic and design

[GitHub repo](https://github.com/antrov/acromegaly/tree/master/PCB)

[Eagle](https://www.autodesk.com/products/eagle/overview) files used to design and manufacture the base PCB with a BLE controller and driver connectors. Besides, board includes an op-amp used to amplify current measurements for ADC, as well as a 8MB Flash memory. 

![PCB Design](https://raw.githubusercontent.com/antrov/acromegaly/master/docs/pcb.png) ![Schematic](https://raw.githubusercontent.com/antrov/acromegaly/master/docs/schematic.png)

## BLE controller (nRF51)

[GitHub repo](https://github.com/antrov/acromegaly-nrf51)

ANSI C code developed for the nRF51 MCU and based on its SDK. The brain of a desk controller, exposes interface for receiving commands from Bluetooth Low Energy and to broadcasts informations like: 
* current height, 
* target height, 
* movement state and direction, 
* current power 

Configured to compile with wide available and free toolchains.

## BLE client (iOS)

[GitHub repo](https://github.com/antrov/acromegaly-ios)

Swift iOS application used to present visually state of the desk and control it remotely.

* auto scanning and connecting to dedicated Acromegaly BLE device
* visual representation of current and requested desk height
* setting exact height of a desk
* swipe gesture to set bounding positions
* storing of the favourites positions

![iOS Client App](https://raw.githubusercontent.com/antrov/acromegaly-ios/master/docs/height.gif) ![iOS Client App](https://raw.githubusercontent.com/antrov/acromegaly-ios/master/docs/favs.gif)