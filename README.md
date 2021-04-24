# HomeAutomation-guides


## Flash OpenMQTTGateWay on a Sonoff R2 v1.0
1. Put the switch on the Sonoff to OFF
2. Solder/connect the sertial to ttl on the 4pin: GND, RX, TX, VCC. RX and TX need to ve inverted between sonoff and the TTL adapter
3. Follow the Direct mod from [here](https://github.com/xoseperez/espurna/wiki/Hardware-Itead-Sonoff-RF-Bridge---Direct-Hack), no need to use a resistance if you are careful
4. While plugin the Adapter to your computer, press the reset button for 5s
5. Use [FlashESP8266](https://github.com/letscontrolit/ESPEasy/releases) with the `sonoff-rfbridge-direct-firmware.bin`[OMG](https://github.com/1technophile/OpenMQTTGateway/releases). Place it in the same folder as the Flash tool.
6. Select the right com port, firmware, flash
7. Flash, when it's done, it say its done, if not, verify the reset button was pressed during plugin and that RX/TX is inverted. 
8. Remove usb and put it again will trigger the restart
9. All activity led are turned off, initial setup only to configure wifi and mqtt broker, other reboot will not allow this. In this case, clear the esp setting

To clear the settings : Flash http://www.pratikpanda.com/wp-content/uploads/2016/05/blank_1MB.zip
