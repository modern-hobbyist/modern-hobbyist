MCU: Was going to do [STM32G474CETx](https://www.st.com/resource/en/datasheet/stm32g474cb.pdf), but it didn't have enough pins (with the LCD) so going to upgrade to the [STM32G474RETx](https://www.st.com/resource/en/datasheet/stm32g474cb.pdf)
- [Unified Daughter Board](https://unified-daughterboard.github.io/#/?id=unified-daughterboard)
	- Rather than an on-board USB C and ESD protection
	- Required Molex PICOEZMATE 4 CIRCUIT 300MM cables and connectors though, which are a little tricky to order.
	- Can order in bulk with custom sizes from [Alibaba manus](https://www.alibaba.com/product-detail/Customized-Molex-EZmate-to-Molex-EZmate_1600697379284.html)
- Switches: Going to design for KS-33 AND MX combined
	- Implemented by overlapping the footprints. It will cause some DRC errors, but it should be functional even with an LED. Pretty much requires a plate for stability though since the holes will be overlapping and not the proper size all the time.
- Keycaps: 
	- Need something with a little bit of flexibility for the thumb keys anyways.
- Case:
	- All aluminum or Aluminum top and polycarbonate bottom
		- I like the idea of the internal electronics being semi-visible like on my DOIO macropad
- Plate:
	- Gasket mount with poron gaskets
		- Double sided gaskets for extra softness, and noise absorbtion
- Layout: 
	- Mostly ANSI 105, but the arrow keys are tucked below palm, thumb cluster in place of spacebar, and some macro keys off to the side
- Standoffs:
	- Designed for M2 screws. Top side would be countersunk into the plate, bottom would not be (under the PCB). 
	- 3.5mm standoffs for gateron or MX normal profile keycaps
	- For KS33, it might make more sense to use a 1.3mm shim with a bolt and nut that goes all the way through the plate and PCB.
		- Or skip the standoffs entirely and just go with thin foam or nothing


# Two Variants
## Gateron Normal/Cherry
### Important Dimensions
- `3.5mm` between Plate and PCB
- `1.5mm` plate thickness
### Sound Tuning
- `3mm` Poron foam between plate and PCB (Plate Foam)
- 2 x `1.5mm` Poron just below the PCB for socket noise cancelling (Case Foam)

## KS-33
### [Important Dimensions](https://www.reddit.com/media?url=https%3A%2F%2Fi.redd.it%2Fgateron-ks-33-low-profile-2-0-stem-length-v0-53pz6mgld2ye1.jpg%3Fwidth%3D1577%26format%3Dpjpg%26auto%3Dwebp%26s%3Db72538ae57b3c330196c13bdc993d41572008f79)
- `1.3mm` between Plate and PCB
- `1.2mm` Plate Thickness
### Sound Tuning
- `1mm` poron foam between plate and PCB (Plate Foam)
- `1.5mm` poron foam below PCB (Case Foam)