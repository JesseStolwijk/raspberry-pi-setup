# raspberry-pi-setup

## Install from scratch

### Write OS to SD card

1. Install (raspberry Pi imager)[https://www.raspberrypi.org/software/]
2. Run raspberry pi imager app
3. Select Raspberry pi os lite (32-bit) os
4. Write the os to the SD card

### Set headless pi config

1. Open SD card in file explorer
2. Create a file named `ssh` in the root folder
3. Set the SSID and secret in the `wpa_supplicant.conf` file
4. Copy `wpa_supplicant.conf` file to the root folder
