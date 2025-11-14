# sendit

ESP32 based tank level sender monitor.

# REV C Todo

* test serial out over usb / jtag port.
* bom
* jlc placement

# REV C Changelog

* switch back to ads1115
* remove adc vref circuit
* scale all outputs to 2.048v instead of 3.3v
  * voltage dividers for 30v and 5v
  * 4-20ma shunt resistor: 100 ohm
* removed the rtc clock crystal
* added 3.3v to 5.0v buffer for ws2818 led
* switch to green leds for power
* add test points for 3.3v, 5.0v, 24v, gnd, sda, scl, etc.
* all test points -> 1.5x0.7
* change piezo to passive + add diode Huaneng QMB-09B-03
* Add a buck converter to the EXT port go to from 12/24 to 5v to power the esp32
  * Should have a jumper to enable/disable power from this port
  * can be used as power only or as reference or both
* move pluggable terminal blocks down 0.5mm
* changed to smt boot/reset buttons
* changed to solder jumper for adc vref selection
* add 2 mounting holes for pcb to case bottom (M2.5)
* switch to SMTSO3080CTJ for 4 mounting holes to case top
* switch to MT3608B for 24v boost converter
* added QWIIC header
* removed usb to serial and usb hub for super simple esp32-s3
* removed jumper for ext power selection