# Switcher 2.0 – 2 Channel WiFi Open Source Switch
This is fork from [this project](https://github.com/hborisov/switcher_pcb).
I've added support for two independent relays, two buttons and DS18B20 digital thermometer. 
It is compatibile with [Sonoff-Tasmota](https://github.com/arendst/Sonoff-Tasmota) firmware.

## Disclaimer
:warning: This device is meant to connect to AC MAINS. Be careful, if you have no experience, ask someone who has to assist you.

## Design
The board size is 46x46mm it shoud fit into standard electrical wall junction box where it is meant to be installed.

## Connections
Connections are very simple. 
1. Connect AC mains L, N to power line.
2. Connect your devices to OUT_1 and OUT_2. Maximum output power output is 400W. It is enough for light sources. It should not be used for wall sockets. For outputs above 200W consider attaching heatsinks to BT136's to dissipate heat.
3. Connect BTN_1 and BTN_2 to momentary buttons, notice that there is no high voltage on these buttons.

## Programming WiFi module
Board is designed to work with ESP8266 module ESP-01S, this is simplest and cheapest ESP module. Unfortunatelly you cannot program module in place, as there is no space for required pinheader. You should flash chip with [Sonoff-Tasmota](https://github.com/arendst/Sonoff-Tasmota) firmware and choose Sonoff Generic device. You need to program module only once, then you can update via web interface.

## Sensor
There is pinheader where you can connect 1-Wire DS18B20 digital thermometer. It uses BTN_1 pin so you can't use both DS18B20 and BTN_1.
