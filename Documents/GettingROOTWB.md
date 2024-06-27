# Getting ROOT - Wifi Board
- The firmware on the device is a plane old linux with DropbearSSH and adb as services, but default is to have these service turned off.

  
Create a new folder in your home directory, cd in to the new directory and clone the lateset version of rkbin 
```
$ mkdir eufy
$ cd eufy
$ git clone https://github.com/rockchip-linux/rkbin.git
```
- Open up you l70 to expose the wifi-board.  
- Remove the small plastic cover under the lid to expose the debug micro USB port.
![GitHub Image](https://github.com/spoonieau/Tetrodotoxin/blob/main/Images/usbdebug.jpg)  
- Get a good quallity USB-A to micro USB cable
- The RockChip RK3308 and have two recovery boot modes MaskRom and Gadget mode. Bord needs to be in Gaget mode to get acces to the storage.
- While the unit is powered off and holding down holding down 'SW1RESET' button, plug in the usb cable in to the pc and the usb micro debug port. The low LED will lite up take finger off the 'SW1RESET'   button.  
![GitHub Image](https://github.com/spoonieau/Tetrodotoxin/blob/main/Images/WifiBoardBoot.jpg)
