# can_around
Play around with CAN bus using micropython and MCP chips on ESP modules

[![micropython](https://img.shields.io/badge/Micro-python-417DAE.svg)](http://docs.micropython.org/en/latest/)

[Arduino Mega](./doc/ArduinoMEGA2560pinout.png)

[Modules connection](./doc/connection.jpg)

![](https://www.rs-online.com/designspark/rel-assets/dsauto/temp/uploaded/githubpin.JPG)



## Setting up USBTinyISP support in Ubuntu for flashing Arduino
```sh
sudo nano /etc/udev/rules.d/99-USBtiny
```
Then paste
```
SUBSYSTEM=="usb", SYSFS{idVendor}=="1781", SYSFS{idProduct}=="0c9f", GROUP="users", MODE="0666"
```
or
```
SUBSYSTEM=="usb", ATTR{idVendor}=="1781", ATTR{idProduct}=="0c9f", GROUP="adm", MODE="0666"
```
into the new file. Write it out by pressing `Ctrl-O` and `Ctrl-X` to exit.
```sh
sudo usermod -a -G plugdev YOURUSERNAME
sudo service udev restart
sudo udevadm control --reload-rules
```
Insert the USBtinyISP again.

## Useful links
* [HABR VAG](https://habr.com/en/post/442184/)
* [Arduino simple communication](https://www.electronicshub.org/arduino-mcp2515-can-bus-tutorial/)
* [! MCP CAN utils](https://vimtut0r.com/2017/01/17/can-bus-with-raspberry-pi-howtoquickstart-mcp2515-kernel-4-4-x)
* [! Installing Python-CAN for Raspberry Pi](https://skpang.co.uk/blog/archives/1220)
* [Python CAN Raspberry Pi](https://python-can.readthedocs.io/en/master/)
* [[quick-guide] CAN bus on raspberry pi with MCP2515](https://www.raspberrypi.org/forums/viewtopic.php?t=141052)
* [CAN2Ethernet](http://lnxpps.de/rpie/)
* [How to Connect Raspberry Pi to CAN Bus](https://www.hackster.io/youness/how-to-connect-raspberry-pi-to-can-bus-b60235)
* [pyobd](https://github.com/peterh/pyobd)
* [piobd](https://www.instructables.com/id/OBD-Pi/)