# Model254e
Files for 254e Quad Control Voltage Processor


<b>Updating Firmware</b>
* Install Arduino IDE v1.5.8 [here] (https://www.arduino.cc/en/main/OldSoftwareReleases).
* Power down cabinet, carefully remove module, leaving it connected to the cabinet.
* Connect a micro USB cable between the module and your computer.
* Power up the cabinet.
* Using a Command Prompt, go to the bossac directory: C:\Program Files (x86)\Arduino\hardware\tools.
* Download the firmware file to the directory.
* Run `listComPorts -v`
* Confirm that the module was found: 
```
			Searching for COM ports...
			COM3 - Arduino LLC (www.arduino.cc) - USB\VID_2341&PID_003E&MI_00\6&36C3CEB1&0&0000 
			Found 1 port	
```
	</li>
	<li>Press the ERASE button on the module.</li>
	<li>Press the RESET button on the module (or cycle power.)</li>
	<li>Again, run <font size="-1" face="Courier New">listComPorts -v</font>. <br/>
		Confirm that the module was found, and take note of the COM port: <br/>
		<font size="-1" face="Courier New">
			Searching for COM ports...<br/>
			<b>COM4</b> - Arduino LLC (www.arduino.cc) - USB\VID_03EB&PID_6124\5&1DB486CD&0&2<br/>
			Found 1 port	<br/>
		</font>
		(If nothing found, press ERASE again. Repeat until the module appears.)
	</li>
	<li>Load the firmware using this command:<br/>
		<font size="-1" face="Courier New">
			bossac -e -w -i -d -v -U true -p=<i>com_port</i> -b <i>firmware_filename</i><br/>
		</font>
		Where <font size="-1" face="Courier New"><i>com_port</i></font> is the COM port noted in the previous step, and 
		<font size="-1" face="Courier New"><i>firmware_filename</i></font> 
		is the name of the firmware file you downloaded. <br/>
		Example: 
		<font size="-1" face="Courier New">
			bossac -e -w -i -d -v -U true -p=COM4 -b Model254eV30.1.cpp.bin<br/>
		</font>
	</li>
	<li>Power down the cabinet, replace the module, then power up the cabinet. </li>
	<li>Press and hold the remote enable button on the module to display the firmware version on the preset manager.</li>
</ul>
