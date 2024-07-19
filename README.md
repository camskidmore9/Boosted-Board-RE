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

Links:
https://embetronicx.com/tutorials/microcontrollers/stm32/bootloader/stm32-firmware-update-over-the-air-fota-wireless-firmware-update/
https://www.senzmate.com/tech-blogs/firmware-upgrade/
https://forum.microchip.com/s/topic/a5C3l000000MdiYEAS/t382729
https://www.infineon.com/dgdl/Infineon-AN214896_Over_the_Air_(OTA)_Firmware_Update_Procedure_for_Bluetooth_Low_Energy_(BLE)_Devices-ApplicationNotes-v03_00-EN.pdf?fileId=8ac78c8c7cdc391c017d0d28900b6369

https://ww1.microchip.com/downloads/en/DeviceDoc/ATWINC1510-Host-Image-Download-User-Guide-DS50002806B.pdf
https://www.instructables.com/CSR-Bluetooth-Module-Programming/
https://venutech.ca/bbteardown
https://foreverboosted.co/
https://www.rapid7.com/blog/post/2019/04/30/extracting-firmware-from-microcontrollers-onboard-flash-memory-part-3-microchip-pic-microcontrollers/
https://microchip.my.site.com/s/article/16-bit-PIC--Configuration-and-working-of-PGEC-and-PGED-pins
https://developerhelp.microchip.com/xwiki/bin/view/software-tools/ides/x/debugging/view-set-configuration-bits/
https://medium.com/@johnathanchiu1065/side-project-series-reverse-engineering-the-boosted-board-remote-ceda4c30a74a
https://github.com/TypeStrong/atom-typescript/issues/547
https://forum.universal-devices.com/topic/41939-zse42-ota-firmware-update/
https://docs.nordicsemi.com/bundle/ncs-latest/page/nrf/samples/bluetooth/throughput/README.html
https://www.infineon.com/dgdl/Infineon-AN214896_Over_the_Air_(OTA)_Firmware_Update_Procedure_for_Bluetooth_Low_Energy_(BLE)_Devices-ApplicationNotes-v03_00-EN.pdf?fileId=8ac78c8c7cdc391c017d0d28900b6369
https://ww1.microchip.com/downloads/en/DeviceDoc/dsPIC33CK256MP508-Family-Data-Sheet-DS70005349E.pdf
https://mu.microchip.com/16-bit-bootloaders-using-mcc-device-side
https://www.microchip.com/en-us/software-library/dspic33-pic24-bootloader
https://ww1.microchip.com/downloads/en/DeviceDoc/40001772C.pdf
https://forum.microchip.com/s/topic/a5C3l000000MdiYEAS/t382729
https://www.microchip.com/en-us/products/wireless-connectivity/over-the-air-updates
https://medium.com/@ps.sujith/decompile-and-recompile-apk-using-apktool-beginners-guide-4ad03c2c5b8f
https://www.reddit.com/r/Android/comments/11852r/how_to_modify_an_apk/
https://xdaforums.com/t/guide-index-how-to-modify-an-apk.4208093/
https://www.unix.com/homework-and-coursework-questions/253223-convert-ascii-text-crlf.html
https://www.diyaudio.com/community/threads/csr8675-programming-guide-w-software-and-tons-of-csr-info.349336/
https://forum.microchip.com/s/topic/a5C3l000000MKIdEAO/t308091
https://www.instructables.com/CSR-Bluetooth-Module-Programming/
https://beambreak.org/articles/known_firmware_versions/
https://medium.com/@jasjot784/how-to-extract-source-code-of-an-apk-using-apktool-b5f601383ab
https://stackoverflow.com/questions/64284171/decompile-kotlin-source-code-from-apk-file
https://github.com/dariuszseweryn/RxAndroidBle/tree/master-rxjava1/rxandroidble/src/main/java/com/polidea/rxandroidble
https://medium.com/@elementalistbtg/android-bluetooth-api-all-you-need-to-know-d9225a84754
https://www.reddit.com/r/boostedboards/comments/fe0j3m/alrighty_folks_its_time_to_come_together_with/
https://github.com/KaneCheshire/remotely
https://github.com/rscullin/beambreak/pull/9
https://beambreak.org/
https://web.archive.org/web/20210122051530/https://saveboosted.com/
https://www.reddit.com/r/boostedboards/comments/i6zgtt/esc_manual_update_progress/
https://www.reddit.com/r/boostedboards/comments/ohg3lg/boosted_firmware_update_manually/
https://foreverboosted.co/faq#company
https://forum.esk8.news/t/flipsky-vx4-update-vs-no-update/68367
https://theboostedguys.com/
https://www.reddit.com/r/boostedboards/comments/uhkfq6/the_boosted_guys_our_boosted_board_esc_upgrade/
https://www.eevblog.com/forum/microcontrollers/reading-eeprom-data-from-pic/
https://forum.microchip.com/s/topic/a5C3l000000MYTrEAO/t362603
https://x.com/johnathanchewy/status/1745144074405806264?ref_src=twsrc%5Etfw%7Ctwcamp%5Etweetembed%7Ctwterm%5E1752595923551592633%7Ctwgr%5E972c15f8b85acd4d41ebc1dd2c146e15207d2426%7Ctwcon%5Es3_&ref_url=https%3A%2F%2Fcdn.embedly.com%2Fwidgets%2Fmedia.html%3Ftype%3Dtext2Fhtmlkey%3Da19fcc184b9711e1b4764040d3dc5c07schema%3Dtwitterurl%3Dhttps3A%2F%2Ftwitter.com%2Fjohnathanchewy%2Fstatus%2F17525959235515926333Fs3D20image%3D
https://hackaday.com/2021/04/24/taking-reverse-engineering-to-the-skies-cheap-drone-gets-px4-autopilot/
https://t.co/79DGFTChT1
https://github.com/johnathanchiu/boosted-project
https://endless-sphere.com/sphere/threads/boosted-boards-reverse-engineered-development.56839/
https://www.cl.cam.ac.uk/~sps32/mcu_lock.html
https://forum.microchip.com/s/topic/a5C3l000000MWoLEAW/t356185
https://hackaday.com/tag/microchip-pic/
https://forum.microchip.com/s/topic/a5C3l000000MJ02EAG/t303094
https://hackaday.com/2011/06/27/bunnies-archives-unlocking-protected-microcontrollers/
http://www.piclist.com/techref/microchip/crackpic.htm
http://www.piclist.com/techref/scenix/crack.htm
https://forum.microchip.com/s/topic/a5C3l000000MUDxEAO/t346241
https://resources.altium.com/p/give-them-no-quarter-preventing-pic-microcontroller-code-from-being-duplicated
https://anee.me/reversing-programmable-interface-controllers-e835c0471ebb?gi=f8f53685334f
https://ww1.microchip.com/downloads/aemDocuments/documents/OTH/ProductDocuments/ReferenceManuals/dsPIC33-PIC24-FRM-Enhanced-CPU-DS70005158C.pdf
https://wiki.newae.com/Tutorial_A9_Bypassing_LPC1114_Read_Protect
https://forum.newae.com/t/crack-code-protection/1445
https://www.reddit.com/r/microcontrollers/comments/rtjtms/where_do_i_start_reverse_engineering_a/
https://www.microchip.com/en-us/product/dspic33ep512gm710
https://forum.microchip.com/s/topic/a5C3l000000MesbEAC/t387196
https://ragnarsecurity.medium.com/reverse-engineering-bare-metal-kernel-images-part-2-6a52a4afa3ef
https://www.infosecinstitute.com/resources/iot-security/iot-security-fundamentals-reverse-engineering-firmware/
https://www.instructables.com/Understanding-ICSP-for-PIC-Microcontrollers/


