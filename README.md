# Model254e
Files for 254e Quad Control Voltage Processor


## Updating Firmware
* Install Arduino IDE v1.5.8 [here] (https://www.arduino.cc/en/main/OldSoftwareReleases).
* Power down cabinet, carefully remove module, leaving it connected to the cabinet.
* Connect a micro USB cable between the module and your computer.
* Using a Command Prompt, go to the bossac directory: C:\Program Files (x86)\Arduino\hardware\tools.
* Download the firmware file to the directory.
* Power up the cabinet.
* Run `listComPorts -v`
* Confirm that the module was found: 
```
			Searching for COM ports...
			COM3 - Arduino LLC (www.arduino.cc) - USB\VID_2341&PID_003E&MI_00\6&36C3CEB1&0&0000 
			Found 1 port	
```
* If the module was not found, stop here and troubleshoot your connection and Arduino installation. Do not proceed until the problem is resolved.
* Press the ERASE button on the module.
* Press the RESET button on the module (or cycle power.)
* Again, run `listComPorts -v`
* Confirm that the module was found, and take note of the COM port: 
```
			Searching for COM ports...
			`*`*COM4`*`* - Arduino LLC (www.arduino.cc) - USB\VID_03EB&PID_6124\5&1DB486CD&0&2
			Found 1 port	
```
* If nothing found, press ERASE again. Repeat until the module appears.
* Load the firmware using this command:
```
			bossac -e -w -i -v -b -U true -p=com_port firmware_filename
```

Where `com_port` is the COM port noted in the previous step, and `firmware_filename` is the name of the firmware file you downloaded. 

Example: 

```
			bossac -e -w -i -v -b -U true -p=COM4 Model254eV30.1.cpp.bin
```		
* Power down the cabinet, replace the module, then power up the cabinet. 
* Press and hold the remote enable button on the module to display the firmware version on the preset manager.
