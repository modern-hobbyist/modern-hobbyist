I took apart the shaft to reverse engineer the wiring and this is what I found:
1. The TV stand's controller has a 6 pin connector to the actual motor
2. Inside the motor, is a ZYT45JS-2
3. The ZYT45JS-2 has two pins for Motor connector 1 and Motor connector 2
4. 4 remaining pins are:
	1. Gnd
	2. 5v (confirmed it's 5v)
	3. Data
	4. Data
5. The two data lines are likely hall effect sensor outputs for reading rotation to have an idea of where the actual lift is at as well as determining if it has stalled.

Bypassing the controller and making one of my own:
1. Will need a high power motor controller (L298n won't cut it)
2. Will need a current sensor for checking if motor is stalled
3. Will need an Arduino or similar to control everything and read Hall Effect inputs
4. A voltage converter, the HE sensors seem to run on 5v.

