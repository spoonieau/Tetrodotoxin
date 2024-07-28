# Tetrodotoxin
Eufy L70 robot vacuum research. 

![GitHub Image](Images/eufyl70.jpg)

The eventual aim is to build a custom frimware using [Yocto](https://www.yoctoproject.org/ "The Yocto Project") and extend the functionality of the unit, add more storage, bt and gamepad support, also to make the unit stanalone "without the need of the eufy app and cloud network connection" . 

In its stock configuration L70 is a [tuya](https://www.tuya.com "tuya") based device using Linux firmware 
```
(Linux 4.4.143 aarch64 (gcc version 6.3.1 20170404 (Linaro GCC 6.3-2017.05))).
```
## Guides
[Networking Info](https://github.com/spoonieau/Tetrodotoxin/blob/main/Documents/Network.md "Networking Info")     
[Serial Console - WifiBoard](https://github.com/spoonieau/Tetrodotoxin/blob/main/Documents/SerialConsoleWB.md "Serial Console WifiBoard")   
[Dumping Firmware - WifiBoard](https://github.com/spoonieau/Tetrodotoxin/blob/main/Documents/DumpingFirmwareWB.md "Dumping Firmware WifiBoard")   
[Getting ROOT - WifiBoard](https://github.com/spoonieau/Tetrodotoxin/blob/main/Documents/GettingROOTWB.md "Getting ROOT WifiBoard")  
[LDRobot LD00 - Lidar](https://github.com/spoonieau/Tetrodotoxin/blob/main/Documents/LDRobotLD00Lidar.md)

The unit comprises of two control PCB boards and one Lidar. 
## Wifi Board
![GitHub Image](Images/WifiBoard.jpg)
This board contains
- RockChip RK3308. 
- Realtek RTL8188F 802.11b/g/n Wifi.
- EMST M15T2G16128A -2G DDR3.
- EMST F59L1G81LB - 128M NAND.
- Populated Uart2 port. 
- Two Push buttons labled 'SW1 RESET' and 'SW2'.
- A unpopulated micro-usb named USB1.
- Connection for the LDRobot LD00 Lidar.
- Connection to an external micro USB debug port. 

## Function Board 
![GitHub Image](Images/FunctionBoard.jpg)
This board contains
- GigaDevice GD32F10x (GD32F103-VBT6) Arm 32-bit MCU.
- Battery connection, power disbrution and charging circuts.
- All of the units functions come from this board.
- Populated five pin debug port.

## TODO
- Get debug port on Function Board working. Data Sheet says its a 'Serial wire JTAG debug port (SWJ-DP)' but no luck.   
- Workout how the two PCB talk to each other, issue comands etc.   
- Workout how the programs control the L70 (input-event-daemon, config_node, event_hub, onboard_ui, slam_pose_provider, navigator, carrier, task_manager, time_server_tactics, network_proxy, idle_task).  
- Build a working Yocto image for the L70.  
