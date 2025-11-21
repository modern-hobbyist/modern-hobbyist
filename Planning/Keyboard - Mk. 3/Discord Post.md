**Mist** is my take on a full size keyboard, but with some upgrades I carried over from my second keyboard build, **Hermod**.

[Full Project Video](https://youtu.be/R__24k-nADY)
## Features

- **2.2" LCD Display**: Shows keyboard state, stats, and any fun animations I come up with.  
- **Thumb Clusters Instead of a Spacebar**: The giant spacebar is such a waste of space, and I loved the thumb clusters from my split board.  
- **Unified Daughter Board Connector**: Moves all the ESD and over-voltage protection off the main PCB and allows for more interesting case designs.  
- **Per-Key RGB Lighting**: A more powerful MCU means I finally have the horsepower for more detailed RGB animations.  
- **KS-33 and MX/Gateron Hot-Swap Support**: Use either KS-33 low-profile switches or standard MX and Gateron switches.  
- **Macro Keys**: Nobody actually uses the function row as intended, so I turned it into macros. The bottom rows can also be almost entirely macro-based thanks to the thumb clusters.  
- **QMK Firmware**: Fully programmable and customizable.  
- **Standard QWERTY Layout and Keymap**: The layout everyone already knows.

## Specifications

- **Microcontroller**: STM32G474RETx  
- **Display**: 2.2" LCD (320x240 resolution) per half  
- **Lighting**: SK6812 Mini RGB LEDs

## Project Resources

- [KiCAD Projects](https://github.com/modern-hobbyist/aesir/tree/main/mist-udb) 
    - Contains KiCad projects, the BOM, and additional instructions.
- [PCBWay Project](https://www.pcbway.com/project/shareproject/Custom_Mechanical_Keyboard_7a40c23a.html)
- [Project Write-up](https://www.modhobbyist.com/projects/)
- [Wiki](http://wiki.modhobbyist.com/Projects/0003%20-%20Project%20Mist/01%20-%20Overview.html)
- [3d Models](https://www.printables.com/model/1486920)

## Firmware

- [My QMK Fork](https://github.com/modern-hobbyist/qmk_firmware)
- [My QMK Userspace](https://github.com/modern-hobbyist/qmk_userspace)