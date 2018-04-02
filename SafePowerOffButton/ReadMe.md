To not corrupt and destroy my SD card by just disconnecting power when I am done reminiscing, I am using a button connected to a spare GPIO to initiate a shutdown script.

I used code that I found from <a href="https://github.com/TonyLHansen/raspberry-pi-safe-off-switch/blob/master/python/shutdown-led-simple.py" target="_blank">TonyLHansen's GitHub</a>. I modified it to use GPIO 26 for the button and GPIO 27 for the LED. 

First you need to create the python code</br>
<b><i>nano shutdown-led-simple.py</i></b>

Then copy/paste the shutdonw-led-simple.py and save it.

If you don't have python installed yet, then you can install it with:</br>
<b><i>sudo apt-get install python3-pip</i></b>

Then you will need to install GPIOZero:</br>
<b><i>sudo apt install python3-gpiozero</i></b>

After that, you can test it with:</br>
<b><i>python3 shutdown-led-simple.py</i></b>

When you know it works, we need it to automatically run at boot. To do that we have to add the following to the etc/rc.local file before the exit 0; instruction. To do that first open the etc/rc.local to edit it:</br>
<b><i>sudo nano /etc/rc.local</i></b>

Then scroll to the bottom and add this just before the <b>exit 0</b></br>
<b><i>(sleep 10;python3 ~pi/shutdown-led-simple.py)&</i></b>

Then reboot and test it out.  
