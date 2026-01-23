# Rev D TODO

* lm74700 reverse polarity on VEXT
* remove pesd3.3v on adc line
* 1k -> 4.7k on the adc input line
* pull in the new esp32-s3 schematic w/ bigger ldo
* wrong p/n for leds - change to green
* 5v + 24v leds still way too bright - check resistor values and change.
* add more thermal gnd vias for regulators
* ideal diode ORing setup on 24v->5v output and USB 5v output
  * Wuxi Maxinmicro MX74610SS (external fet)
  * LM74700 (external fet, p/n re-use)
* usb 5v output -> ideal diode.
* bulk cap on 5v
* expansion header -> bottom and change to smt
* change to bigger / higher amperage chip for 5v to 24v
  * TI TPS55340 -> modern, internal, async -> easy peasy <winner>
  * TI TPS40211 -> modern, external, async kinda complicated
  * TI TPS43061 -> synchronous / more complicated
* change to bigger / higher amperage chip for 24v to 5v
  * DIODES AP64350 (3.5A)
  * DIODES AP64200 (2A)
* add bottom test points to important input / outputs
* update all p/ns per bom/ff