# BB-RS485
Beaglebone black device tree overlay for RS485 (MAX485)

# USAGE
Connect pin 11 (uart4 rx) to RO.
Connect pin 13 (uart4 tx) to DI.
Connect pin 27 (gpio3 19) to DE and RE.

Make sure you have a recent enough kernel to have the patched RS485 support.
3.8.13-bone39 or higher should be enough.

# COMPILE AND INSTALL
dtc -O dtb -o BB-RS485-00A0.dtbo -b 0 -@ BB-RS485-00A0.dts 
sudo cp BB-RS485-00A0.dtbo /lib/firmware

