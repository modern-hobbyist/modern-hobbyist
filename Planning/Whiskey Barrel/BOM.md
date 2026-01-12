TV Lift: https://a.co/d/alf75nU
Whiskey Barrel: 53 Gallon, standard size, provided by Cedar Ridge distillery


# Electronics BOM
| Item | Part | Purpose | Link |
|------|------|---------|------|
| Microcontroller | Arduino Nano (ATmega328P) | Main control, hall counting, ramp, button logic | https://store.arduino.cc/products/arduino-nano |
| Motor Driver (H-Bridge) | BTS7960 / IBT-2 43A DC Motor Driver | Drives 18V ~5A motor safely (huge headroom) | https://www.amazon.com/dp/B07D2C8P6M |
| DC-DC Converter | LM2596 Buck Converter (18V→5V) | Powers Arduino + hall sensors | https://www.amazon.com/dp/B07VVXF7YX |
| Current Sensor (optional) | ACS758-050B Hall Current Sensor | Detects stall / overload by current spike | https://www.pololu.com/product/1180 |
| Momentary Button | Panel-mount SPST NO pushbutton | Single control input | https://www.adafruit.com/product/1442 |
| Pull-up Resistors | 10kΩ ¼W (2×) | Hall sensor open-collector pullups | https://www.digikey.com/en/products/detail/yageo/MFR-25FBF52-10K/1346 |
| TVS Diode (optional) | SMBJ33A | Protects against motor supply spikes | https://www.digikey.com/en/products/detail/littelfuse-inc/SMBJ33A/762104 |
| Fuse | 10A ATC Blade + Holder | Motor supply protection | https://www.amazon.com/dp/B000CQ0QXM |
| Connector (optional) | Molex Micro-Fit 3.0 6-pin | Clean mate to motor harness | https://www.digikey.com/en/products/detail/molex/0436450600/252516 |
