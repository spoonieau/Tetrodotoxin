# Getting ROOT - Wifi Board
- The firmware on the device is a plane old linux with DropbearSSH and ADB as services, but default is to have these service turned off. Get the following tools.   
```
$ sudo pacman -S dropbear android-udev android-tools
```
- The init scripts are looking to see if a file is present in the userdata partition, if present the service starts.
- Mount the userdata image dumped previously [Dumping l70 firmware](https://github.com/spoonieau/Tetrodotoxin/blob/main/Documents/DumpingFirmwareWB.md "Dumping l70 firmware")  
  ```
  $ sudo mkdir /mnt/eufy
  $ sudo mount <location to image>/userdata.img /mnt/eufy
  $ cd /mnt/eufy
  $ sudo touch /cfg/init.d/adbd
  $ sudo touch /cfg/init.d/dropbear
  $ cd /
  $ sudo umount 
  ```
       
