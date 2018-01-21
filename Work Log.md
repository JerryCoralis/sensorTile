# Internet of Things - progress log

## Raspberry pi
issues with formatting usb in linux
issues using NOOBS to install raspbian, tarball was corrupt even though sha256sum showed valid file integrity

resolved by flashing raspbian stretch image file


formating usb: http://qdosmsq.dunbar-it.co.uk/blog/2013/06/noobs-for-raspberry-pi/
https://www.garron.me/en/go2linux/format-usb-drive-fat32-file-system-ubuntu-linux.html

flashing stretch:
https://www.youtube.com/watch?v=ana7uz0l728

## challenges
1. ssh the raspberry pi. How to use laptop to interface with it
https://www.raspberrypi.org/documentation/remote-access/ssh/
1. how to get sensor tile to talk with RaspPi using bluetooth
2. how to access that data from sensor tile
3. how to get that data to cloud

## connecting R\pi to sensor tile via bluetooth
ST address: C0:7A:31:30:18:4D
