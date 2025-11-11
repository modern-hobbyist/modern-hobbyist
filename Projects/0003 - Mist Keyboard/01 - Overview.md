---
title: Mist Keyboard
layout: home
nav_order: "0"
parent: Projects
---
# Mist

**Mist** is my take on a full size keyboard, but with some upgrades I carried over from my second keyboard build--**Hermod**. Furthermore, this is the UDB version of **Mist**, which stands for Unified Daughter Board

Aside from the UDB connector and the lack of USB-C/on-board ESD protection circuitry, this keyboard is functionally identical to the base **Mist** keyboard.

## Why?

1. First of all, I'm addicted to designing custom keyboards now, so jot that down.
2. I have two children now, and while I love my split keyboard (and my children), I'm more often than not holding a child. Typing with one hand is 100 times more difficult and time consuming on a split.
3. Related to above, I wanted a keyboard that would appeal to the non-split community, but also incorporate all the features I loved mose about my split build.

## Features

- **2.2" LCD Display**: A 2.2" LCD Display to show keyboard state, stats, and any fun animations I can think of.
- **Thumb Clusters in Place of Spacebar**: I loved the thumb clusters from my split keyboard and the giant spacebar is such a waste of...well, space!
- **Connector for Unified Daughter Board**: A Unified Daughter Board extracts all the ESD and over-voltage protection from the main PCB and allows for more complex case shapes.
- **Per-Key RGB Lighting**: With a more powerful MCU, I have the brains for many more RGB animations!
- **KS-33 + MX/Gateron Normal Profile Hot-Swappable Switch Sockets**: Support for either KS-33 low-profile or MX style (Cherry or Gateron Normal profile) switches.
- **MACRO KEYS**: Let's be honest, nobody uses the `function` keys as they were intended, so instead, I made them all macros. Additionally, the bottom two rows can become almost exclusively macros since the thumb clusters accomplish what the bottom row does on a standard keyboard.
- **QMK Firmware**: Fully programmable and customizable using QMK.
- **Standard QWERTY Layout and Keymap**: The layout we all grew up learning to type on!

## Specifications

- **Microcontroller**: STM32G474RETx
- **Display**: 2.2" LCD (320x240 resolution) per half.
- **Lighting**: SK6812 Mini RGB LEDs.

## Firmware

Since this is a custom keyboard, it's generally assumed that you'll want to customize the firmware as well. This board is compatible with QMK and I've put together a basic starter firmware in my fork of the main QMK repository. You'll be able to learn more from the QMK Docs or Discord than I can teach you in a single README file, but my fork, and my QMK Userspace should be good resources to help you get your own custom firmware going. 

However, if you happen to love the way I've got my firmware set up, you can find the most recent binary in the releases section of my Userspace:

- [QMK Docs](https://docs.qmk.fm/)
- [My QMK Fork](https://github.com/modern-hobbyist/qmk_firmware)
- [My QMK Userspace](https://github.com/modern-hobbyist/qmk_userspace)

Since this keyboard has an LCD, the odds are you'll want to put something on there. If I'm correct in thinking that, below you can find a more detailed walk through of how to get a custom keymap PNG for your display:

- [[03 - Creating Keymap Image for LCD|Flashing a custom image to your LCD]]

## License

This project is licensed under the MIT License. See the [LICENSE](../LICENSE) file for details.

## Acknowledgments

- The QMK community for their amazing firmware.
- Adafruit for the GFX library support.
- Inspiration from the mechanical keyboard enthusiast community.

---

For more information, check out the [Modern Hobbyist YouTube channel](https://www.youtube.com/ModernHobbyist) for videos about this project!

> Also, please let me know in an issue or on Discord if there are issues with this board or the supplementary files so I can get them updated!
