---
title: Instructions
layout: home
nav_order: "1"
parent: Split Keyboard - Mk. 1
---
# Split Keyboard Mk. I - Instructions

----
<span class="label label-yellow">This Page is a Work In Progress | Check Back Soon</span>

<img src="../../img/hermod-mk-1/thumbnail-5.png" alt="hermod-thumbnail"/>
This is my very first split keyboard build ever, and while it's far from perfect, it was an amazing learning experience. 

>**Disclaimer:**  
This DIY split keyboard PCB was designed for personal use and is shared as-is. While it works well for me, it's not a professionally validated design—there ~~may~~will be be imperfections or quirks. If you decide to build it, please do so at your own risk. Double-check everything, and make modifications as needed. Happy building!

# Requirements
To complete this build, you'll need the following:
### Required
- 3d Printer or ability to get 3d printed parts
- Soldering Iron
- Computer

### Optional
- Hot air soldering station
	- Alt. is to order your PCB's assembled

# 3D Models
I have included a link to the 3D models on Printables for you to download and print, but in case the tolerances aren't correct for your printer, I have also included the Fusion360 project so you can adjust them yourself. 
- [Printables](https://www.printables.com/model/1303280-custom-split-keyboard-case)
- Fusion360 Projects
	- Right - https://a360.co/4jo1lfW
	- Left - https://a360.co/3HjPXUH
	- Numpad - https://a360.co/3FjKqgo

# PCB

<span class="label">Use this link to get $5 off your first order!</span> - https://pcbway.com/g/F41R62

- [PCBWay Project](https://www.pcbway.com/project/shareproject/Modular_Split_Mechanical_Keyboard_7a8f16f0.html) - You can order it directly from here, and even have it assembled.
- [KiCAD Project](https://github.com/modern-hobbyist/aesir/tree/main/hermod) - In case you need to reference the PCB or Schematic during the soldering process.
- [PCB BOM](https://www.digikey.com/en/mylists/list/8VSL0OSHL7) - If anything is missing from this list please contact me on Discord so I can update it!

# Hardware BOM

| Item                          | Description                                                   | Unit Price | Extended Price USD | Link |
|------------------------------|---------------------------------------------------------------|------------|---------------------|------|
| USB_C_Receptacle_USB2.0      | HRO Koreaparts M-14 mid-mount USB-C 2.0                      | $1.65      | $1.65               | [Link](https://www.lcsc.com/product-detail/USB-Connectors_Korean-Hroparts-Elec-TYPE-C-31-M-14_C223907.html) |
| Magnetic Pogo Connectors     | 4 sets of male+female                                         | $1.91      | $7.64               | [Link](https://www.aliexpress.us/item/3256807450239540.html?spm=a2g0o.order_list.order_list_main.5.65051802pm4kbe&gatewayAdapt=glo2usa) |
| 2.2" LCD Display - No Touch  | This keyboard uses the 2.2 No touch                          | $4.85      | $9.70               | [Link](https://www.aliexpress.us/item/2255800032844649.html?spm=a2g0o.order_list.order_list_main.105.65051802pm4kbe&gatewayAdapt=glo2usa) |
| Choc Hot Swap Sockets - 1u   | These are for both the 1u and 1.5u switches.                 | $12.88     | $12.88              | [Link](https://www.aliexpress.us/item/3256805821531402.html?spm=a2g0o.order_list.order_list_main.59.65051802pm4kbe&gatewayAdapt=glo2usa) |
| Kailh Choc Low Profile Switches | The actual switches that plug into the Hot Swap sockets above. | $54.82     | $54.82              | [Link](https://www.aliexpress.us/item/3256804880270570.html?spm=a2g0o.order_list.order_list_main.90.22b51802WAWGdO&gatewayAdapt=glo2usa) |
| 1u Keycaps                   |                                                               | $25.06     | $50.12              | [Link](https://www.aliexpress.us/item/3256804371784456.html?spm=a2g0o.order_list.order_list_main.181.4e5218021PwPwR&gatewayAdapt=glo2usa) |
| 1u Homing Keycaps            |                                                               | $3.49      | $3.49               | [Link](https://www.aliexpress.us/item/3256804593704786.html?spm=a2g0o.order_list.order_list_main.80.22b51802fUmZ3v&gatewayAdapt=glo2usa) |
| 1.5u Keycaps                 | 2 Pack                                                        | $3.55      | $24.85              | [Link](https://www.aliexpress.us/item/3256804593704786.html?spm=a2g0o.order_list.order_list_main.80.22b51802fUmZ3v&gatewayAdapt=glo2usa) |
| M3x8mm Bolts                 | M3x8mm                                                        | $0.12      | $2.64               | [Link](https://boltdepot.com/Product-Details?product=13635) |
| M3x3mm Heat Set Inserts      | M3x3mm - Pack of 50                                           | $0.12      | $5.95               | [Link](https://www.adafruit.com/product/4256) |
| Poron Foam - 3mm             | 50X15X0.3CM                                                   | $5.69      | $5.69               | [Link](https://www.aliexpress.us/item/3256804497716681.html?spm=a2g0o.order_list.order_list_main.112.263f18022PcLB8&gatewayAdapt=glo2usa) |

# Building

### PCB Assembly

<span class="label label-yellow">TODO</span>
### Assembly

<span class="label label-yellow">TODO</span>

### Firmware

Please keep in mind that you will still need to customize the firmware to some degree. The current layout of this keyboard isn't for everyone, and the displays show images of my Keymap. 

- [Vanilla Hermod Firmware](https://github.com/modern-hobbyist/qmk_firmware/tree/modhobbyist/keyboards/aesir/hermod) 
	- Base Firmware to get you started. No display animations or sleep timers. Pretty basic, but gives you full control over what you do with the firmware.
- [Userspace Valhalla Firmware](https://github.com/modern-hobbyist/qmk_userspace/tree/main/keyboards/aesir/hermod/keymaps/valhalla)
	- Pretty much what I run normally, without my custom macros. 

If you find yourself needing to customize the displays, macros, activity timeouts or anything else QMK Specific, either check out the QMK Docs or reach out to someone on the QMK Discord.

- [QMK Docs](https://docs.qmk.fm/)
- [QMK Discord](https://discord.com/invite/qmk)

You can also reach out on my [Discord](https://discord.gg/68WXGsjqJp), though I likely won't be much help to you, as I barely scraped this together.

### Updating LCD Layer Images
To summarize the steps to update the layer images for the LCDs:

1. Update the Photoshop file for the layer you want to update (in `qmk_userspace/layouts`
2. Export Photoshop file as PNG
3. Convert the PNG to a QGF File format using `qmk painter-convert-graphics` command
4. Overwrite or add the new QGF file to your `keymap.c` and render it when/where you want.

In the keymap.c file in my QMK Userspace, I include a few different files for each of the keymap layers I use. For now, I only use 2 layers, but with a split keyboard that comes out to 4 image files that need drawn to the LCDs. The current files are included at the top of `keymap.c` and are as follows:

```
#include "./graphics/left-base-layout.qgf.h"
#include "./graphics/right-base-layout.qgf.h"
#include "./graphics/left-1-layout.qgf.h"
#include "./graphics/right-1-layout.qgf.h"
```

If you want to replace the images with your own custom layout, there are some Photoshop files in the `qmk_userspace/layouts` directory that you can edit. I found it easiest to edit the keymap in Photoshop or another editor of your choice to set the text for each key on each layer, then export it as a PNG.

Once you have updated the Photoshop files to have the proper text for each key in the layer you're working on and exported them as PNG's, move them to the `qmk_userspace/layouts` directory (proper file management is important!) and open up a `terminal`.

In your terminal, navigate to that `qmk_userspace/layouts` directory and run the following command to convert the PNG to a QGF format (results in a .c and a .h file).

```
qmk painter-convert-graphics -i base/left-base-layout.png -o output -f pal4
```

Replace the input (in this case `base/left-base-layout.png`) with the PNG you created earlier, and replace the output (in this case the `output` directory inside `qmk_userspace/layouts`) with the output directory you want to use. Or keep it the same as me and simplify your life.

The above command will convert the input file to a `.c` and `.h` file with the same name as the input PNG and move it to the output file you specified. 

From there, you can import the 
# Resources
## Absolute TOP resources:
- [Keyboard Layout Editor](https://www.keyboard-layout-editor.com/)
- [Keyboard Atelier](https://kbatelier.org/)
- [QMK Firmware](https://docs.qmk.fm/),  [QMK Discord](https://discord.com/invite/qmk)
- [Noah Kiser's STM32F072 Template](https://github.com/NCKiser/STM32F072_template)
- [AIO3 Plate Generator](https://kbplate.ai03.com/)
- [KBPlacer Plugin for KiCAD](https://github.com/adamws/kicad-kbplacer)

## Everything else
Below is a list of every single link I saved during the building of this keyboard. It might not be complete, and it might actually be a little bit overwhelming, but they were each helpful to me in some way, so I figured better safe than sorry and included them all!

- [https://github.com/ruiqimao/keyboard-pcb-guide?tab=readme-ov-file#setting-up](https://github.com/ruiqimao/keyboard-pcb-guide?tab=readme-ov-file#setting-up)
- [https://github.com/tmk/kicad_lib_tmk](https://github.com/tmk/kicad_lib_tmk)
- [https://github.com/tmk/keyboard_parts.pretty](https://github.com/tmk/keyboard_parts.pretty)
- [https://github.com/egladman/keebs.pretty](https://github.com/egladman/keebs.pretty)[https://www.reddit.com/r/MechanicalKeyboards/comments/5nzpd2/guide_how_to_make_your_own_keyboard_pcb/](https://www.reddit.com/r/MechanicalKeyboards/comments/5nzpd2/guide_how_to_make_your_own_keyboard_pcb/)
- [https://i.imgur.com/ajqxJWz.png](https://i.imgur.com/ajqxJWz.png)
- [https://www.youtube.com/watch?v=7azQkSu0m_U](https://www.youtube.com/watch?v=7azQkSu0m_U)
- [https://www.youtube.com/watch?v=iznKltVU1yw](https://www.youtube.com/watch?v=iznKltVU1yw)
- [https://www.youtube.com/watch?v=kGKN8SGkUD0](https://www.youtube.com/watch?v=kGKN8SGkUD0)
- [https://github.com/Zambumon/SKUF](https://github.com/Zambumon/SKUF)
- [https://maxkeyboard.com/ansi-layout-custom-color-cherry-mx-keycap-set.html](https://maxkeyboard.com/ansi-layout-custom-color-cherry-mx-keycap-set.html)
- [https://yuzukeycaps.com/](https://yuzukeycaps.com/)
- [https://amzn.to/3XczB5T](https://amzn.to/3XczB5T)
- [https://keyboard-tools.xyz/](https://keyboard-tools.xyz/)
- [https://docs.qmk.fm/custom_quantum_functions](https://docs.qmk.fm/custom_quantum_functions)
- [https://github.com/getreuer/qmk-keymap?tab=readme-ov-file](https://github.com/getreuer/qmk-keymap?tab=readme-ov-file)
- [https://plate.keeb.io/](https://plate.keeb.io/)[https://discord.com/channels/728571839529353216/1040846204856193154/1040846268945145866](https://discord.com/channels/728571839529353216/1040846204856193154/1040846268945145866)
- [https://hackaday.com/2023/08/07/all-about-usb-c-example-circuits/](https://hackaday.com/2023/08/07/all-about-usb-c-example-circuits/)
- [https://github.com/daprice/keyswitches.pretty?tab=readme-ov-file](https://github.com/daprice/keyswitches.pretty?tab=readme-ov-file)
- [https://kicanvas.org/](https://kicanvas.org/)
- [https://www.etsy.com/listing/549370705/custom-sublimation-transfers-sizes-up-to?ref=yr_purchases](https://www.etsy.com/listing/549370705/custom-sublimation-transfers-sizes-up-to?ref=yr_purchases)
- [https://github.com/Maximillian/keycap-set-templates?tab=readme-ov-file](https://github.com/Maximillian/keycap-set-templates?tab=readme-ov-file)
- [https://www.reddit.com/r/olkb/comments/1bvyo0j/oled_screen_wont_work_qmk/](https://www.reddit.com/r/olkb/comments/1bvyo0j/oled_screen_wont_work_qmk/)
- [https://github.com/kitspace/awesome-electronics](https://github.com/kitspace/awesome-electronics)
- [https://blog.keeb.io/getting-the-iris-ce-compact-edition-ready-for-you/](https://blog.keeb.io/getting-the-iris-ce-compact-edition-ready-for-you/)