## Desired Features
- 2.2" LCDs
- Arrow keys Tucked Below palm
- Thumb keys slightly closer to the center of hand
	- Also, thinking of switching to a 3 key thumb cluster with arched keys instead of a 2x2 grid (the top thumb keys were hard to reach with my thumbs)
	- Before
		![[screenRecording-000186.png]]
	- After
		![[screenRecording-000185.png]]
- sk6803 mini-e LED instead of the sk6812 mini-e 
	- Lower power draw, but almost un-noticeable brightness loss
- North Facing Switches
	- I like the shine through keycaps from Tai-hao that are used on the ZSA Voyager, but they have the shine through dot (or legend) on the north side of the keycap. So rotating all the switches 180º would improve that shine through look.
- 

### Issues with V1
- ~~No pullup resistor on the split comm data line. 5.1k resistor to 3.3v (or 5v if the data pin is 5v tolerant)~~
- Should wire the serial comm to a USART RX pin, or better yet, do Full Duplex instead of half duplex comms
- Need to make sure leds are on a free PWM pin (using one of the timers that isn't being used by something else)
- Need to make sure the LCD SPI is free
- Need to make sure the LCD backlight PWM pin is on a free timer as well.
- Not enough ram or storage for many animations


### Things to keep an eye out for when designing
- Don't use `systick` timer (tim2)
- Make sure MCU doesn't need an external clock, use one if it does
