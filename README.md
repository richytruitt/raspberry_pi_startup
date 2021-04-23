# raspberry_pi_startup

## Raspberry Pi headless auto connect to wifi and start ssh

When running a raspberry pi using a headless UI, there isn't an easy way to get connected to it if you don't have a monitor and keyboard handy. Instead, you can follow these steps to make sure the raspberry Pi automatically connects to your network, and starts the SSH tool

1. Download the headless Raspbian Lite distro from [here](https://www.raspberrypi.org/software/operating-systems/)
2. unzip the contents and you should have a disc image file (.img). Use a tool, in my case I used Etcher, to burn the .img file to an SD card that you plan to use for the Pi
3. Clone repo or download the files. Modify the wpa_supplicant.conf file to add your network name and password. 
4. When the image is finished being burned to the SD card, keep the card in the computer, and navigate to the root of the boot directory. 
5. Place both the ssh, and the wpa_supplicant.conf file at the root. 
6. Remove the card from the computer safely, and insert into the Raspberry Pi. Allow it to boot and you should be able to find it on the network to connect to ssh with using the root creds pi and raspberry as the username and password respectively