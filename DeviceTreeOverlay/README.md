For my device tree overlay, I decided to use Mode 6 of the DPI settings. Using mode 6 allows me to have 6 bits red, 6 bits green and 6 bits blue.
The benefit of using Mode 6 instead of Mode 5 is that it frees up GPIO 18 and 19 to be used for PWM0 and PWM1 which are needed for stereo audio from the Pi Zero. 

The Pi needs a .dtbo file for it to load the device tree overlay. and how you create it is by using the device tree compiler (dtc). 

My instance of retropi did not have dtc already installed, so i had to install it with pip 
