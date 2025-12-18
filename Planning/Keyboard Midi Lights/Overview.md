I'd like to revisit the Keyboard LED project I did a few years ago, but make it plug and play for users by converting to a custom PCB that is plug and play, maybe with a touch screen display or some buttons to configure your settings.

# Hardware
- RP2040 MCU 
- USB C for power and firmware flashing
- RGB LEDs (144pix/m)

# Firmware
- Automatically dims LEDs based on total estimated amperage
- Multiple customizable modes
- Reads Midi input, sustain pedal, etc...
	- Adjust the fade speed based on pedal
	- Adjust brightness if mute pedal is pressed

I'd be able to program it in ArduinoIDE or Platformio fairly easily if using an STM32 MCU or VSCode + Platformio for RP2040.

