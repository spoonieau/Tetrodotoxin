# Dumping Firmware - Wifi Board
- Create a new folder in your home directory, cd in to the new directory and clone the latest version of rkbin. 
```
$ mkdir eufy
$ cd eufy
$ git clone https://github.com/rockchip-linux/rkbin.git
```
- Open up you L70 to expose the wifi-board.  
- Remove the small plastic cover under the lid to expose the debug micro USB port.
![GitHub Image](https://github.com/spoonieau/Tetrodotoxin/blob/main/Images/usbdebug.jpg)  
- Get a good quallity USB-A to micro-USB cable
- The RockChip RK3308 has two recovery boot modes MaskRom mode and Gadget mode. Board needs to be in Gaget mode to get acces to the storage.
- While the unit is powered off and holding down holding down 'SW1RESET' button, plug in the usb cable in to the pc and the usb micro debug port. The board LED will lite up, take your finger off the 'SW1RESET' button.  
![GitHub Image](https://github.com/spoonieau/Tetrodotoxin/blob/main/Images/WifiBoardBoot.jpg)

- If successful lsusb will dispaly something like.  
```
$ lsusb
Bus 001 Device 007: ID 2207:330d Fuzhou Rockchip Electronics Company USB download gadget
```
Now run the 'upgrade_tool' from the rkbin folder, cloned previously.
```
$ cd rkbin
$ cd tools
$ ./upgrade_tool
```
- If the upgrade_tool finds the rk3308 correctly.
```
List of rockusb connected
DevNo=1 Vid=0x2207,Pid=0x330d,LocationID=13     Mode=Loader
Found 1 rockusb,Select input DevNo,Rescan press <R>,Quit press <Q>:
```
- Now we need to have a look at the partition layout, copy and past the layout in to a txt file.
```
$ ./upgrade_tool pl
Partition Info(gpt):
NO  LBA        Size       Name
01  0x00002000 0x00001000 uboot
02  0x00003000 0x00001000 trust
03  0x00004000 0x00000800 misc
04  0x00004800 0x00001000 sysdata
05  0x00005800 0x00006800 recovery
06  0x0000c000 0x00005800 boot
07  0x00011800 0x0000e000 rootfs
08  0x0001f800 0x0000a000 oem
09  0x00029800 0x0000c5df userdata
```
- So now lets dump everything.
```
./upgrade_tool RL 0x00002000 0x00001000 uboot.img
./upgrade_tool RL 0x00003000 0x00001000 trust.img
./upgrade_tool RL 0x00004000 0x00000800 misc.img
./upgrade_tool RL 0x00004800 0x00001000 sysdata.img
./upgrade_tool RL 0x00005800 0x00006800 recovery.img
./upgrade_tool RL 0x0000c000 0x00005800 boot.img
./upgrade_tool RL 0x00011800 0x0000e000 rootfs.img
./upgrade_tool RL 0x0001f800 0x0000a000 oem.img
./upgrade_tool RL 0x00029800 0x0000c5df userdata.img
```
- You have now dumped everything from the rom of the device. You can now mount any *.img and have a bit of a poke around.  

- Output of file ran on the image files.  
```
file uboot.img
uboot.img: data

file trust.img
trust.img: data

file misc.img
misc.img: data

file sysdata.img
sysdata.img: Linux rev 0.0 ext2 filesystem data (mounted or unclean), UUID=e03b3c71-aff4-4a98-90b5-b49a70aee023

file recovery.img
recovery.img: Android bootimg, kernel (0x10008000), ramdisk (0x11000000), second stage (0x10f00000), page size: 2048

file boot.img
boot.img: Android bootimg, kernel (0x10008000), second stage (0x10f00000), page size: 2048

file rootfs.img
rootfs.img: Squashfs filesystem, little endian, version 4.0, zlib compressed, 23471679 bytes, 3061 inodes, blocksize: 131072 bytes, created: Mon Jul  1 15:19:15 2019

file oem.img
oem.img: Linux rev 0.0 ext2 filesystem data (mounted or unclean), UUID=aa408385-73cd-4bff-9665-1aa40af2822b

file userdata.img
userdata.img: Linux rev 0.0 ext2 filesystem data (mounted or unclean), UUID=1195d710-8ab5-451f-97fa-c335c48a2eb3
```


