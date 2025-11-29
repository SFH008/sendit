# Changelog

## REV C

### 🔧 ADC & Analog Front-End
- Switched back to **ADS1115** ADC.
- Removed the **ADC VREF circuit** and added a **solder jumper** for VREF selection.
- Standardized all analog scaling to **2.048 V** reference (instead of 3.3 V).
- Added voltage dividers for **30 V** and **5 V** input ranges.
- Set **4–20 mA shunt resistor** to **100 Ω**.
- Added **pull-up resistors** on ADS1115 ALERT pin.

### ⚡ Power & Regulation
- Added a **buck converter** on the EXT port for **12/24 V → 5 V** to power the ESP32.
  - Includes a jumper to **enable/disable EXT-port power**.
  - EXT port may now be used as **power-only**, **reference-only**, or **both**.
- Added **3.3 V ↔ 5.0 V buffer** for WS2818 LED.
- Switched to **green LEDs** for power indication.
- Removed the **USB-to-serial** and **USB hub** for a simplified ESP32-S3 design.

### 🧩 Connectors & I/O
- Added **QWIIC header**.
- Moved pluggable terminal blocks **down 0.5 mm**.
- Removed jumper for EXT power selection.

### 🧪 Test Points
- Added test points for **3.3 V**, **5.0 V**, **24 V**, **GND**, **SDA**, **SCL**, and others.
- Standardized all test points to **1.5×0.7 mm**.

### 🔊 Piezo & Indicators
- Switched to **passive piezo** and added diode (**Huaneng QMB-09B-03**).

### 🧱 Mechanical & Layout
- Changed upper mounting holes to **SMTSO3080CTJ** hardware.
- Switched to **SMT boot/reset buttons**.
- Removed RTC **clock crystal**.
- Switched boost converter to **MT3608B** for 24 V generation.

