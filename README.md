# AzusChromebookC202
Upgrade an Asus Chromebook C202S or C202SA to Ubuntu Linux 

This includes all the HW and software instructions necessary to upgrade your Asus Chromebook model C202S or C202SA to Ubuntu Linux.

Link to a good general overview:  https://docs.mrchromebox.tech/docs/getting-started.html

Data:
Asus c202s   Model c202sa—ys02   intel model 7265ngw   Chipset: Intel Braswell  HW ID: Terra

Model:  ASUS Chromebook C202SA	HW ID: TERRA	YEar: 2016	Processor: Intel Braswell Firmware: Required Full Firmware [UEFI]
Chrome OS:   103.0.5060.53 – 64 bit  - ELO Jun 2022  hw id Terra   4gb ram, 16 gb ssd

Choose, download and burn (Use Rufus) install to a 10+GB USB:   https://releases.ubuntu.com/jammy/

HW Installation:
Remove 10 screws on the back
Flip over tablet, open the cover and gently pry the keyboard cover off 
Remove R/W screw (see JPG)
 
Reassemble

Enable developer mode Developer Mode: https://docs.mrchromebox.tech/docs/boot-modes/developer.html

Run the Firmware Utility Script: https://docs.mrchromebox.tech/docs/fwscript.html
To download and run this script under ChromeOS, enter: <ctrl><alt><t>   then type: shell
Issue the following:   cd; curl -LO mrchromebox.tech/firmware-util.sh && sudo bash firmware-util.sh
Reboot the machine

Hit <Esc>  for boot menu
Insert your Ubuntu USB
Follow installation instructions.
Select minimal GUI install, do not include open office.
