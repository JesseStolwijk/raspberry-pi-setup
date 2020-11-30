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

### Assign a .local domain

Since almost all networks use DHCP to assign IP addresses it can be quite frustrating to lookup the IP every time you want to connect to the raspberry pi. To reolve this issue I like to assign the `<hostname>.local` adress to my pi so that I can connect the pi easily.

First off ssh into the pi and update all packages:

```
    sudo apt-get update

    sudo apt-get upgrade
```

Install the avahi mDNS implementation:
`sudo apt-get install avahi-daemon`

When the installation you should be able to reach the pi via the `<hostname>.local` adress. The default hostname is `raspberrypi`, so you should be able to reach the pi over `raspberrypi.local` if you havent changed the hostname.

Lets try to ssh to the pi using the .local domain:
`ssh pi@raspberrypi.local`
`pi@raspberrypi.local's password:`

Nice it works!
