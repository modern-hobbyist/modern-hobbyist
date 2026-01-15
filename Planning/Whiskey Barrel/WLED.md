Since I wanted to add LEDs, spinning this project up as a WLED instance gives me the best of both worlds:
1. WLED for network managed LED control
2. WLED Usermod for the motor control
	1. Allows for pin inputs/outputs, sensors, motors, etc...
	2. Can adjust settings via the WLED interface in a browser
		1. E.g. can adjust the shutoff current for when the motor has reached the end of it's track
		2. Can adjust the pin assignments, the steps/mm from the hall effect sensors, etc...

# Compiling the usermod
1. Configuring WLED in Platformio was the most difficult part for me
	1. Using VSCode with the Platformio plugin
2. Had to download WLED via Git
	1. Open the root WLED (not wled00) directory in VSCode
3. Go into the `platformio.ini` file
4. Adjust which build targets you want -- I am using the `esp32dev` board, so I disabled everything but that
5. Find that build target in the `platformio.ini` file and add the custom usermod `usermod_motor_controller`
6. Also add the `adafruit/Adafruit INA219@^1.2.3` module
   ```
   [env:esp32dev]
		board = esp32dev
		platform = ${esp32_idf_V4.platform}
		platform_packages = ${esp32_idf_V4.platform_packages}
		build_unflags = ${common.build_unflags}
		custom_usermods = usermod_motor_controller
		build_flags = ${common.build_flags} ${esp32_idf_V4.build_flags} -D WLED_RELEASE_NAME=\"ESP32\" #-D WLED_DISABLE_BROWNOUT_DET
		              -DARDUINO_USB_CDC_ON_BOOT=0 ;; this flag is mandatory for "classic ESP32" when building with arduino-esp32 >=2.0.3
		lib_deps = ${esp32_idf_V4.lib_deps}
		  adafruit/Adafruit INA219@^1.2.3
		monitor_filters = esp32_exception_decoder
		board_build.partitions = ${esp32.default_partitions}
		board_build.flash_mode = dio
   ```
7. Click the upload button at the very bottom of the screen in the blue bar
   ![[screenRecording-000954.png]]