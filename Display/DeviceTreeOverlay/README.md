For my device tree overlay, I decided to use <b>Mode 6</b> of the DPI Output Format. Using mode 6 allows me to have 6 bits red, 6 bits green and 6 bits blue. The benefit of using Mode 6 instead of Mode 5 is that it frees up GPIO 18 and 19 to be used for PWM0 and PWM1 which are needed for stereo audio from the Pi Zero. 

The Pi needs a .dtbo file for it to load the device tree overlay. How you create it is by using the device tree compiler (dtc). So the first thing you need to do is make sure you have dtc installed 

<b><i>sudo apt-get install device-tree-compiler</i></b>

To compile the blob file myself. I first created the <b>dpi18mode6.dts</b> file in the <b>/boot/</b> directory.</br>
Then I used dtc to compile it into the .dtbo file with this command:

<b><i>sudo dtc -W no-unit_address_vs_reg -@ -I dts -O dtb -o /boot/overlays/dpi18mode6.dtbo /boot/dpi18mode6.dts</i></b>

Once that is created you then have to add <b>dtoverlay=dpi18mode6</b> to the boot/config.txt file so the pi knows to load it. You can copy my config.txt from this github repo.
