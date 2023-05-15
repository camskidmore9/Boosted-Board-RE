# Boosted-Board-RE
Reverse Engineering on a Boosted Board V2 firmware. Research on board, etc


Links:
https://medium.com/@rxseger/spi-interfacing-experiments-eeproms-bus-pirate-adc-opt101-with-raspberry-pi-9c819511efea

https://ivanorsolic.github.io/post/hardwarehacking1/

https://www.flashrom.org/Bus_Pirate

https://www.pentestpartners.com/security-blog/faster-eeprom-firmware-reads-use-a-pi/

https://konukoii.com/blog/2018/02/13/lifting-firmware-with-the-bus-pirate/

https://payatu.com/using-rasberrypi-as-poor-mans-hardware-hacking-tool/

PIC Extraction Guide:
https://www.rapid7.com/blog/post/2019/04/30/extracting-firmware-from-microcontrollers-onboard-flash-memory-part-3-microchip-pic-microcontrollers/

Apparently app points to:
boosted-app.com:9000

This is a registered domain so buying this domain and hosting the update is not an option. Owned by someone using DomainsByProxy.
Expires: 2023-08-05T12:19:46Z

9/28: After many attempst to pull firmware, it appears the read is hanging while trying to extract the firmware. Upon reasearching this topic, this link was found:
http://dangerousprototypes.com/forum/index.php?topic=8688.0

Need to update BusPirate firmware
^Not necessary, eventually managed to work via soldering pins to the chip in question.


5/14: Successful extracting of supposed firmware was completed a while ago. Info from inside boosted (acquired via discord from friend who worked there) shows that targeted chip was a logging/debug chip and did not house firmware. Info may still be useful to someone but not me. Upon more looking at the board, it appears that the main firmware can be accessed via PIC program chip on the bottom of PCB. Removal of conformal coating on next idea of main MCU points to big chip with tons of pins.   
    Chip identified as Micrchip dsPIC33EP512 GM710-I/PF
Next step is to map pins on the board to debug pins via continuity and datasheet confirmation.

