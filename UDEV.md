# Name USB Devices
Using this guide you can create a symbolic link to your usb devices

Plug in your devices one-by-one and follow these rules with each device.

With your device plugged in, you can find the device name under something like ```/dev/ttyUSB#``` where # is your number, or ```/dev/sd*``` where * is a alphabetic character. The easiest way to do this for unmounted devices would be ```sudo lshw -short```. Other methods include ```df -h``` and ```lsblk``` for mounted devices. 
```udevadm info --name=/dev/ttyUSB0 --attribute-walk```