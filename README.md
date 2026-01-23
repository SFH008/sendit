# SendIt — Open Hardware ADC Multitool

SendIt is an open-hardware, open-firmware controller designed as a multi use tool for handling various inputs with a focus on DIY marine usage.  It runs on the Yarrboard Framework and provides a clean web UI for configuration, and multiple different APIs for accessing your data.

Built on the **ESP32-S3**, SendIt has 8 channels of 16-bit ADC with 5 different types of configurable input circuits.  With this board, each channel can be individually configured to handle these types of inputs:

* **4-20ma Transducers/Senders:** sender between +VE and GND
* **Positive Switching:** 0-32v, voltage divider acts as pulldown when NC, switch between SIGNAL and +VE
* **Negative Switching:** 1k ohm, top half of voltage divider acts as pullup, switch between SIGNAL and GND
* **0-32v:** simple voltage divider, voltage wired to SIGNAL
* **0-10k ohm:** voltage divider, external resistor wired from SIGNAL to GND
* **0-5v:** simple voltage divider, voltage wired to SIGNAL
* **Thermistor:** 0-10k ohm, wired as normal
* **Raw/Passthrough:** no extra circuitry - wire your own custom circuit

# Hardware

## Controller Board

### Core capabilities:

- ESP32-S3 module with WiFi and USB-C  
- 12–30 V DC input with onboard power regulation  
- Can be powered by USB C or external power input
- 8 x 16-bit ADC channels with 5 selectable circuits
- Selectable sensor VCC voltage for each channel (3.3v, 5v, 24v, external power)
- 30mA resettable fuse on sensor VCC
- I²C expansion (QWIIC connector)
- Unused I/O broken out as 2.54mm pin headers

### Rev C Pinout

![SendIt Rev C Pinout](/diagrams/Sendit%20Pinout%20Rev%20C.png)

### ADC Input Channel

![SendIt Rev C ADC Channel](/diagrams/SendIt%20ADC%20Channel%20-%20Rev%20C.png)