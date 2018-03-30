For my device tree overlay, I decided to use Mode 6 of the DPI settings. Using mode 6 allows me to have 6 bits red, 6 bits green and 6 bits blue.
The benefit of using Mode 6 instead of Mode 5 is that it frees up GPIO 18 and 19 to be used for PWM0 and PWM1 which are needed for stereo audio from the Pi Zero. 

The Pi needs a .dtbo file for it to load the device tree overlay. and how you create it is by using the device tree compiler (dtc). 

My instance of retropi did not have dtc already installed, so i had to install it with pip 

To compile the blob file myself. I first created the dpi18mode6.dts file in the /boot/ directory.</br>
Then I used dtc to compile it into the .dtbo file with this command:

dtc -@ asldf asasd;fkl jas' 

Once that is created you then have to add it to the boot/config.txt file so the pi knows to load it. 
