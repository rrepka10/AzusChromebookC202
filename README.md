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

There is an issue with the audio driver in Ubuntu, make the following changes to fix a high pitch whine 
after about 5 minutes of playing music or video.  Add the following lines to the end of the conf file.

```
sudo vi  /etc/modprobe.d/alsa-base.conf
options snd_hda_intel power_save=0
options snd-hda-intel power_save_controller=N
options snd_sof sof_debug=1
```

Install screen brightness key binding controls with:
```
sudo apt install light
sudo chmod +s $(which light)
```

The use the Ubuntu config screen to set custom key bindings with:

light up :  light -A 20

light down: light -U 20 

Use the audio bindings to bind the volume up/down 

Other suggestions: 

Install a SD card and format it as EXT4

Disable and remove the swap file - saves 2GB or move it to the SD card

Use the symbolic link command ```ln -s targetDir link``` in your home to move data like "Downloads" to the SD card
saving more primary disk space

Use the 
