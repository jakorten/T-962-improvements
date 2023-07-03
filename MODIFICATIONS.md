# Infrared IC Heater T-962

I bought the T-962 by Elektor which already has the following improvements:
 - Paper tape removed and welding blanket installed
 - Earth of socket connected properly to chasis (tested with multimeter)

# Additions
I added a junction DS18B20 cold-junction sensor. Note: you don't need to scape off any PCB layers but can just use the GND pad of other parts (e.g. the 8 pin unsoldered SOIC device). Use your multimeter to see which pins are grounded.

# Programming using a Mac
On the Mac I use homebrew to install lpc21isp:

    brew install lpc21isp

I used the following code to flash the firmware:

    lpc21isp -hex build/T-962-controller.hex /dev/tty.usbserial-A50285BI 57600 11059

To make things easier I also added a panel mounted USB cable to easily attach an external USB cable to a FTDI Serial Adapter (FT232RL USB - TTL Adapter 3.3V).
