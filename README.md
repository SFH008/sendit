# sendit
ESP32 based tank level sender monitor.

# REV C Ideas

* fix resistor values on leds
* case *slightly* interferes with pluggable terminal blocks
* Add a buck converter to the EXT port go to from 12/24 to 5v to power the esp32
  * Use a small chip like LV2841, AP63205, LGS5145, TX4137, LGS5148
  * If AP63206, check out this post: https://github.com/VoronDesign/Voron-Tap/issues/42
  * Should have a jumper to enable/disable power from this port
* switch back to ads1115
* scale all outputs to 2.048v instead of 3.3v?
  * voltage dividers
  * 4-20ma shunt resistor
* change piezo to passive + add diode Huaneng QMB-09B-03
* add test points for 3.3v, 5.0v, 24v, gnd, sda, scl, etc.
* all test points -> 1.5x0.7