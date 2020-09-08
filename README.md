# RTKBaseStation
Base station that are building on top of RTKLIB

This is a BaseStation that are on build on top of the RTKLIB-software. 
Will update with a BOM and a list of component that needed for this is #BOM-folder

The guide can be used for Raspberry Pi 1, Raspberry Pi 2 and also for the Raspberry Pi 3 and also Raspberry Pi Zero. When the instructions are different between the models we will comment that. 

I have done this setup with the Raspberry Pi Zero. 

This is the step I have done:

1. Downloaded the "new" raspberry pi imager and written the Raspbian 32 bit image on the SD-card from here : https://www.raspberrypi.org/downloads/
2. Added a file called ssh in the root directory for the raspberry pi to be able to ssh into it
3. Added a file called wpa_supplicant.conf to add the following lines to direct connect to the my wifi
3a. 
country=US
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1

  network={
      ssid="NETWORK-NAME"
      psk="NETWORK-PASSWORD"
  }
4. Connected the raspberry and login into it with user: pi password: raspberry
5. Run sudo raspi-config
6. Enable the ssh options to be always activated
7. Enable the serial output and disbale the serial console
8. Expand the filesystem to the maximum for the SD-card
