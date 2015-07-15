# odroid-mali-proprietary

Odroid Mali-400 proprietary support libraries.
Hardkernel/Odroid tends to package them as part of bigger packages, which is 
inconvenient when building an linux image from scratch.

On Debian Jessie, these files should be copied to /usr/lib/arm-linux-gnueabihf.
On most other systems, it should be /usr/lib.


## R3P2

The R3P2 binaries were downloaded from
http://dn.odroid.com/MALI400_R3P2/20130429-for-xorg-1.13.3/mali_packages.tar.gz

These packages include a binary for the xf86-video-mali driver. When using a different
version of X11, it needs to be rebuild. The sources can be found at:
http://malideveloper.arm.com/downloads/drivers/DX910/r3p2-01rel4/DX910-SW-99003-r3p2-01rel4.tgz

The xf86-video-mali driver is known to copy the pixel data around quite inefficiently using 
ump for shared memory.

## R4P0

These are hopefully part of
http://www.odroid.in/lubuntu-13.10-xbmc/lubuntu-desktop-13.10-armhf-odroidx2_20140408.img.xz

They can be used with the armsoc X11 driver, which uses DMA-buf for shared memory and should
have higher performance.

## R5P0

Copied from http://builder.mdrjr.net/tools/u3/4412_r5p0_x11.tar.xz
These don't require libUMP anymore. A matching kernel for the X2 can be found at
https://github.com/hardkernel/linux/tree/1130f8761789bfe79de0db2b7f5013ff3eb1f978
