# sendit
ESP32 based tank level sender monitor.

# REV C Ideas

* case *slightly* interferes with pluggable terminal blocks - move them down .5mm
* add 1-2 mounting holes for pcb to case bottom if possible
* switch to SMTSO3080CTJ for 4 mounting holes to case top

# REV C Changelog

* switch back to ads1115
* remove adc vref circuit
* scale all outputs to 2.048v instead of 3.3v
  * voltage dividers for 30v and 5v
  * 4-20ma shunt resistor: 100 ohm
* removed the rtc clock crystal
* added 3.3v to 5.0v buffer to ws2818 led
* switch to green leds for power
* add test points for 3.3v, 5.0v, 24v, gnd, sda, scl, etc.
* all test points -> 1.5x0.7
* change piezo to passive + add diode Huaneng QMB-09B-03
* Add a buck converter to the EXT port go to from 12/24 to 5v to power the esp32
  * Should have a jumper to enable/disable power from this port
  * can be used as power only or as reference or both
