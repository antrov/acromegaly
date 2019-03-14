# Acromegaly PCB

[Eagle](https://www.autodesk.com/products/eagle/overview) files used to design and manufacture the base PCB with a BLE controller and driver connectors. Besides, board includes an op-amp used to amplify current measurements for ADC, as well as a 8MB Flash memory. 

![PCB](https://raw.githubusercontent.com/antrov/acromegaly/master/docs/pcb_1.png)

## Required parts:
* 2mm raster 4x9 connectors
* 2.74mm raster goldpin connectors
* M45PE80 - 8MB FLASH Memory
* LM358 - op-amp for current measurement
* double BTS 7960 as H-Bridge driver - [sample](http://www.alselectro.com/motor-driver-hbridge-43amps-bts7960.html)
* LM3671 3.3V Buck Converter Breakout - 3.3V - step-down power supply from 5V to 3.3V - [sample](https://www.adafruit.com/product/2745)
* nRF51 Core Board - 2mm raster pins - [sample](https://www.waveshare.com/core51822.htm)
* 4x 1MΩ -  SMD 1206 Resitors
* LM393 with slot detector - [sample](https://www.electrokit.com/produkt/modul-med-optisk-lasgaffel/)
* Mask for slot detector - [PDF](https://github.com/antrov/acromegaly/tree/master/PCB/gap_mask.pdf)

## Flashing

During development on DK board, flashing is done by integrated JLink (SEGGER) programmer. In order to flash Acromegaly PCB it is necessary to connect DK VVC/GND instead of LM3671 and SWDIO/SWCLK to dedicated PCB connectors accoriding to [following rules](https://electronut.in/nrf51-dk-external-programming/)

## Slot detector

[Mask PDF](https://github.com/antrov/acromegaly/tree/master/PCB/gap_mask.pdf)

![Slot senor in action](https://raw.githubusercontent.com/antrov/acromegaly/master/docs/slot_sensor.gif)