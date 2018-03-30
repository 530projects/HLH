To use the Pi's GPIO to drive the TFT Display, I use the information I found on this <a href="http://blog.reasonablycorrect.com/raw-dpi-raspberry-pi/">Reasonably Correct</a> blog.

On his blog he has a link to a <a href="https://docs.google.com/spreadsheets/d/15KRhR_ewzdGEeD576rL36FbblRVt5HGhNZakOgW-zg4/edit?usp=sharing">google sheet</a> for how he calculated the <b>dpi_output_format</b> and <b>hdmi_timings</b> values needed in the boot/config.txt file. 

I used his google sheet and also this <a href="https://www.raspberrypi.org/documentation/hardware/raspberrypi/dpi/README.md">raspberrypi.org document</a> to get the values that I used.</br>
I basicaly just changed to mode 6 on the dpi_output_format and changed the clock rate to match that of the adafruit example at the bottom of the raspberrypi.org document.
