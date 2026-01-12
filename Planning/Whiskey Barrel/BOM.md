TV Lift: https://a.co/d/alf75nU
Whiskey Barrel: 53 Gallon, standard size, provided by Cedar Ridge distillery


# Electronics BOM
| Item                      | Part                            | Purpose                                         | Link                                                               |
| ------------------------- | ------------------------------- | ----------------------------------------------- | ------------------------------------------------------------------ |
| Microcontroller           | Arduino Nano (ATmega328P)       | Main control, hall counting, ramp, button logic | https://store.arduino.cc/products/arduino-nano                     |
| Motor Driver (H-Bridge)   | DC Motor Driver                 | Drives 18V ~5A motor safely (huge headroom)     | https://a.co/d/aKubEays                                            |
| DC-DC Converter           | LM2596 Buck Converter (18V→5V)  | Powers Arduino + hall sensors                   | https://www.amazon.com/dp/B07VVXF7YX                               |
| Current Sensor (optional) | ACS758-050B Hall Current Sensor | Detects stall / overload by current spike       | https://a.co/d/ftulnU2                                             |
| Momentary Button          | Panel-mount SPST NO pushbutton  | Single control input                            | https://www.adafruit.com/product/1442                              |
| Connector (optional)      | Molex Micro-Fit 3.0 6-pin       | Clean mate to motor harness                     | https://www.digikey.com/en/products/detail/molex/0436450600/252516 |
