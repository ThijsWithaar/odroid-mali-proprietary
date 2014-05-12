# odroid-mali-proprietary

Odroid Mali-400 proprietary support libraries.
Since hardkernel/Odroid tends to package them as part of bigger packages.
These are the extracted blobs, which can be usefull when building an linux image from scratch

On Debian Jessie, these files should be copied to /usr/lib/arm-linux-gnueabihf
On most other systems, it should be /usr/lib

## R3P2


R3P2 is from
http://dn.odroid.com/MALI400_R3P2/20130429-for-xorg-1.13.3/mali_packages.tar.gz

It requires an X11 driver (xf86-video-mali) which can be found at
http://malideveloper.arm.com/downloads/drivers/DX910/r3p2-01rel4/DX910-SW-99003-r3p2-01rel4.tgz
