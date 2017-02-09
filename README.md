# Model254e
Files for 254e Quad Control Voltage Processor


## Updating Firmware
* Download BOSSA [here](https://sourceforge.net/projects/b-o-s-s-a/files/1.2.1/) and install.
* Download the firmware file.
* Power down cabinet, carefully remove module, leaving it connected to the cabinet.

* Connect a micro USB cable between the module and your computer.

* Power up the cabinet. 
* Run BOSSA.
* Press the Refresh button in BOSSA and confirm that a COM port shows up in the dropdown list. If a COM port does not appear, troubleshoot the USB connection.
* Press the ERASE button on the module.
* Press the RESET button on the module.
* Again press the Refresh button in BOSSA, and this time select the COM port.
* Browse to the firmware file you downloaded.
* Make sure the `Erase All` and `Boot to Flash` boxes are checked (and nothing else).
* Press the Write button in BOSSA to write the firmware to the module.
* Shut down the cabinet, reinstall the module, and power up the cabinet.
* Press and hold Remote Enable to view the firmware version on the preset manager.
