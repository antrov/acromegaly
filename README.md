![Header Image](https://raw.githubusercontent.com/antrov/acromegaly/master/docs/header.png)

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

![PCB Design](https://raw.githubusercontent.com/antrov/acromegaly/master/docs/pcb.png) ![PCB real photo](https://raw.githubusercontent.com/antrov/acromegaly/master/docs/pcb_3.png)

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

## Contact
In case of new issues, concepts or just a will to say hello:

* antrof@gmail.com
* https://www.linkedin.com/in/handr/

## License 

Copyright 2019 Hubert Andrzejewski

This code is distributed under the terms and conditions of the MIT license.

```
Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```