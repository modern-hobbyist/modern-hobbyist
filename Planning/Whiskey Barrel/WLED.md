Since I wanted to add LEDs, spinning this project up as a WLED instance gives me the best of both worlds:
1. WLED for network managed LED control
2. WLED Usermod for the motor control
	1. Allows for pin inputs/outputs, sensors, motors, etc...
	2. Can adjust settings via the WLED interface in a browser
		1. E.g. can adjust the shutoff current for when the motor has reached the end of it's track
		2. Can adjust the pin assignments, the steps/mm from the hall effect sensors, etc...