# PHASE 1 – Hardwarebasis FireBeetle 2 ESP32-C6

## Board
- DFRobot FireBeetle 2 ESP32-C6
- Chip laut Bootlog: ESP32-C6 Revision v0.2
- Flash laut Bootlog: 4 MB
- USB-Port am Mac: /dev/cu.usbmodem1101

## Erfolgreiche Tests
- ESPHome installiert: 2026.5.3
- ESP-IDF v6.0: hello_world Build erfolgreich
- ESP-Matter mit ESP-IDF v5.5.4: light Build + Flash erfolgreich

## Offene Hardwareanalyse
- Exakte Board-Revision
- Pinout
- Onboard-LED / RGB-LED
- Batterieanschluss
- Batteriemessung
- ADC-fähige Pins
- GPIO8 als geschaltete Sensorversorgung

## Onboard-LED
- Beschriftung auf Board: 15/D13
- GPIO: 15
- Arduino-Bezeichnung: D13
- DFRobot-Doku: Default onboard LED pin = 15
- Vermutung für Tests: active HIGH, also HIGH = an, LOW = aus
