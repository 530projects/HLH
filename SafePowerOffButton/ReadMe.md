To not corrupt and destroy my SD card by just disconnecting power when I am done reminiscing, I am using a button connected to a spare GPIO to initiate a shutdown script.

I used code that I found from <a href=https://github.com/TonyLHansen/raspberry-pi-safe-off-switch/blob/master/python/shutdown-led-simple.py target="_blank">TonyLHansen's GitHub</a>. I modified it to use GPIO 26 for the button and GPIO 27 for the LED. 

Once the python script is created in the pi/ directory you can test it with
Python3 sadfasdlfjsalfj/py

When you know it works, we need it to automatically run at boot. To do that we have to add the following to the etc/rc.local file before the exit 0; instruction. 
(sleep 10, pyothon aasdjf.py );  needs deatil.

Then reboot and test it out.  
