# HomeAutomation-guides


## Flash OpenMQTTGateWay on a Sonoff R2 v1.0
1. Put the switch on the Sonoff to OFF
2. Solder/connect the sertial to ttl on the 4pin: GND, RX, TX, VCC. RX and TX need to be inverted between sonoff and the TTL adapter
3. Follow the Direct mod from [here](https://github.com/xoseperez/espurna/wiki/Hardware-Itead-Sonoff-RF-Bridge---Direct-Hack), no need to use a resistance if you are careful
4. Press the reset button while plugin the usb to the adapter, keep pressed for 5s
5. Flash the blank to reset everything : http://www.pratikpanda.com/wp-content/uploads/2016/05/blank_1MB.zip
6. Use [FlashESP8266](https://github.com/letscontrolit/ESPEasy/releases) with the `sonoff-rfbridge-direct-firmware.bin`[OMG](https://github.com/1technophile/OpenMQTTGateway/releases). Place it in the same folder as the Flash tool.
7. Select the right com port, firmware, flash
8. Flash. If failed, verify the reset button was pressed during plugin and that RX/TX is inverted. 
9. Remove usb and put it again will trigger the restart
10. All activity led are turned off, initial setup only to configure wifi and mqtt broker (via wifi on OpenMQTTGateway SSID)
11. After successful configuration,  you can remove the adapter, set the switch to on.
