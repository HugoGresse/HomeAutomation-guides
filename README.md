# HomeAutomation-guides


## Flash OpenMQTTGateWay on a Sonoff R2 (basic)

1. Put the swith on the sonoff to off
2. Solder/connect the sertial to ttl on the 4pin: GND, RX, TX, VCC. RX and TX need to ve inverted between sonoff and the TTL adapter
3. While plugin the Adapter to your computer, press the reset button for 5s
4. Use [FlashESP8266](https://github.com/letscontrolit/ESPEasy/releases) with the sonoff_basic from [OMG](https://github.com/1technophile/OpenMQTTGateway/releases). Note to use the basic sonoff firmware, place it in the same folder as the Flash tool.
5. Select the right com port, firmware, flash
6. Flash, when it's done, it say its done, if not, verify the reset button was pressed during plugin and that RX/TX is inverted. 
7. Remobe usb and put it again will trigger the restart
8. All activity led are turned off, initial setup only to configure wifi and mqtt broker, other reboot will not allow this. In this case, clear the esp setting

To clear the settings : Flash http://www.pratikpanda.com/wp-content/uploads/2016/05/blank_1MB.zip
