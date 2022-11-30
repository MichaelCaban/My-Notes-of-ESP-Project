# My-Notes-of-ESP-Project
School work

### Name of project
The ESP 32 Project

### Purpose
To Create a functioning WIFI PENETRATION TOOL!!!

### Equipment that i used
ESP32-CAM-MB (I did not use the camera for this work)
32GB SD card
A laptop with Windows 11
ESP32 Flash Download Tool V 3.9.3


### Links For Documentation
[Works owner thanks for the help Link](https://github.com/risinek/esp32-wifi-penetration-tool)

### Steps That I Followed
I am a windows user so this will work best if you are on windows
1:
Download all the files from the link above and extract it to the desktop or some where easy to get access to.

2:
Download this [Flash Download Tool and The other 2 tools](https://www.espressif.com/en/support/download/other-tools)

3:
When finished downloading you will need to open it and start the prosses to install it to your Esp32 device

4:
You will then get the option to choose the ESP you will obiously choose ESP 32 option

5:
Soon after you choose the ESP32 you will have to fill out the SPIDownload and will fill it out like so.
(https://user-images.githubusercontent.com/113206250/204481939-edaea826-cf59-4083-90c6-a6585b6da5f7.PNG)
(Note: you don't need the first one)
To get it like this you will need to click the three dots and connect the 3 things in the ESP32 wifi penetration folder
bootloader ; partiton table ; and the actual tool
All of these are found under the build file within the esp32-wifi-penetration-tool-master folder downloaded

6:
To find where the device is connected you will need to search for the port that it is connected to.

7:
You will right click the start menu and look for device manager and the device will be in ports you will be selecting the COM through this.

8:
After all that make sure the device you are installing this to is connected and your holding the reset button that is on the device and start the process.

9:
Once it is completed you may start to open Command Prompt

10:
When comand prompt is opened if not already installed, install python with this [websites directions](https://cyberblogspot.com/how-to-install-esptool-on-windows-10/)

11:
When finnished installing Python or if you already have it you will need to type this 
esptool.py version

12:
[click this link](https://github.com/risinek/esp32-wifi-penetration-tool) and go where it says flash and copy the code it should have an easy scan paste it on the CMD and DO NOT click enter

13:
You will now change the directory of the device which is coded as
cd Where the esp32-wifi-penetration-tool-master folder is

14:
You will then change the Port name to The COM that it was connected to that was in the driver manager.
It will look like this after changes esptool.py -p COM AND THE NUMBER -b 115200 --after hard_reset write_flash --flash_mode dio --flash_freq 40m --flash_size detect 0x8000 build/partition_table/partition-table.bin 0x1000 build/bootloader/bootloader.bin 0x10000 build/esp32-wifi-penetration-tool.bin

15: Now run the command and see it do its magic
(when Activating you will hold down the button that the device has again till done)

### Use the Device

1:
go to the wifi that is connected with the device the defult is
SSID: ManagementAP
Pass: mgmtadmin

2: 
Then go to a brouser and search 192.168.4.1

3:
After wards you can choos what type of attack you want to use to all SSID that is available to the listed ones on the the site 

### What i had trouble with

Problem 1: 
God it was so annoying to configure settings on to this thing you mess up one step and you might not realize what it was till the end.

Problem 2:
For those that are trying to do part 13 i got stuck there and had to manualy insert all the locations to the files that i needed to finaly make a connection.

Problem 3:
If you mess up on step 5 your screwed the entire project up. restart from there and go threw it thouroghly in the end you'll find small issues that can be annoying but fixed
