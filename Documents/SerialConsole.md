# Serial Console Connection
- Using a ```Silicon Labs CP210x UART Bridge```.
- Using picocom ```$sudo pacman -S picocom```.
- Connection.   
  
![GitHub Image](https://github.com/spoonieau/Tetrodotoxin/blob/main/Images/SerialHookup.jpg)

## Picocom Connection Settings
```
port is        : /dev/ttyUSB0
flowcontrol    : none
baudrate is    : 115200
parity is      : none
databits are   : 8
stopbits are   : 1
escape is      : C-a
local echo is  : no
noinit is      : no
noreset is     : no
hangup is      : no
nolock is      : no
send_cmd is    : sz -vv
receive_cmd is : rz -vv -E
imap is        :
omap is        :
emap is        : crcrlf,delbs,
logfile is     : none
initstring     : none
exit_after is  : not set
exit is        : no
```
```
picocom -b 115200 /dev/ttyUSB0
```
## Serial Console Boot Log
```
Terminal ready
R�▒���ij�+�|�:�*;
                 ���*j)"�
                         ���ʯ �,���z�9��j▒�����J���X,J:~
                                                        ��
                                                          ���8�J▒�
                                                                  ����8▒�▒|�Z

                                                                             ��\J▒|
                                                                                   �8�����,���,KR�#

                                                                                                   ��*�����1em����p����əzc��/��t�7;m����Y�觪C��������椨�:▒���������/!��j#;������.�(���
                                                                                                                                                                                      ��������'K��8Y+�*��K����\
                                                                                                                                                                                                                8j▒�"�Z��)
                                                                                                                                                                                                                          ���ꛋ�����
                                                                                                                                                                                                                                   �J)�ʚ��m˲�j�(�'�������\H�▒�����J
                                                                                                                                                                                                                                                                   ���$�+j�9����ZZ���:����
        ��h
           �e��m���
                   jl�c�-�3���lhf�i�
                                    ��lfem���#
                                              �em��[gm���m����;�
                                                                �������
                                                                       ��d���mof�C
le���f�ooh����                                                                    �m��mm
              �mfg�
                   �lm���
                         �lm����ln�Lm�d�
                                        ����lfdfCfno�
                                                     �mg���������mf�l����f������f�����ef������f�����eff�
                                                                                                        ��g�f���df����
                                                                                                                      ��g��
                                                                                                                           �limg�me������
                                                                                                                                         �nM���em��l-d�����
                                                                                                                                                           ���mn��
                                                                                                                                                                  ��menmm��▒�og��
                                                                                                                                                                                 �dl����m�����
                                                                                                                                                                                              �hl��
                                                                                                                                                                                                   �ol9��l���en��
                                                                                                                                                                                                                 �jd
                                                                                                                                                                                                                    �id��m���mn3��-d��olC��l�K�n3��id
                                                                                                                                                                                                                                                     �id��ms�ml�3
                                                                                                                                                                                                                                                                 �K
m��id��ol��lm���ol���m�dLol��mn��ol�                                                                                                                                                                                                                               �mn���
                                    ���L�d����óL�ll���L�lmn�L+dl�L���L�h���l��f�����nl�L�m��������mmo1��l���L���[[    0.074466] console [ttyFIQ0] enabled
    0.074466] console [ttyFIQ0] enabled
[    0.081889] bootconsole [uart0] disabled
[    0.081889] bootconsole [uart0] disabled
[    0.086156] Registered fiq debugger ttyFIQ0
WARNING: suspend_mode_handler: Not support call: 0x4
[    0.103029] vcc_1v8: regulator get failed, ret=-517
[    0.104210] vcc_1v8: supplied by vcc_io
[    0.104868] SCSI subsystem initialized
[    0.105116] usbcore: registered new interface driver usbfs
[    0.105198] usbcore: registered new interface driver hub
[    0.105327] usbcore: registered new device driver usb
[    0.106518] Advanced Linux Sound Architecture Driver Initialized.
[    0.107225] Bluetooth: Core ver 2.21
[    0.107290] NET: Registered protocol family 31
[    0.107302] Bluetooth: HCI device and connection manager initialized
[    0.107322] Bluetooth: HCI socket layer initialized
[    0.107338] Bluetooth: L2CAP socket layer initialized
[    0.107372] Bluetooth: SCO socket layer initialized
[    0.108471] rockchip-cpuinfo cpuinfo: Serial         : 3f2ed2cd6f9e30b2
[    0.108999] clocksource: Switched to clocksource arch_sys_counter
[    0.111394] thermal thermal_zone1: power_allocator: sustainable_power will be estimated
[    0.111723] NET: Registered protocol family 2
[    0.112441] TCP established hash table entries: 2048 (order: 2, 16384 bytes)
[    0.112503] TCP bind hash table entries: 2048 (order: 3, 32768 bytes)
[    0.112559] TCP: Hash tables configured (established 2048 bind 2048)
[    0.112647] UDP hash table entries: 256 (order: 1, 8192 bytes)
[    0.112684] UDP-Lite hash table entries: 256 (order: 1, 8192 bytes)
[    0.112905] NET: Registered protocol family 1
[    0.113710] hw perfevents: enabled with armv8_cortex_a53 PMU driver, 7 counters available
[    0.126623] squashfs: version 4.0 (2009/01/31) Phillip Lougher
[    0.126926] ntfs: driver 2.1.32 [Flags: R/O].
[    0.130337] io scheduler noop registered (default)
[    0.131644] phy phy-ff008000.syscon:usb2-phy@100.0: Failed to get VBUS supply regulator
[    0.135314] dma-pl330 ff2c0000.dma-controller: Loaded driver for PL330 DMAC-241330
[    0.135355] dma-pl330 ff2c0000.dma-controller:       DBUFF-32x8bytes Num_Chans-6 Num_Peri-12 Num_Events-12
[    0.137666] dma-pl330 ff2d0000.dma-controller: Loaded driver for PL330 DMAC-241330
[    0.137705] dma-pl330 ff2d0000.dma-controller:       DBUFF-128x8bytes Num_Chans-8 Num_Peri-20 Num_Events-16
[    0.138049] rockchip-pvtm ff000000.grf:pmu-pvtm: failed to get rst 0 pmu
[    0.138190] rockchip-pvtm ff00c000.syscon:pvtm: failed to get rst 0 core
[    0.139460] Serial: 8250/16550 driver, 5 ports, IRQ sharing disabled
[    0.141548] ff0b0000.serial: ttyS1 at MMIO 0xff0b0000 (irq = 11, base_baud = 5078125) is a 16550A
[    0.142486] ff0e0000.serial: ttyS4 at MMIO 0xff0e0000 (irq = 12, base_baud = 5078125) is a 16550A
[    0.143046] [drm] Initialized drm 1.1.0 20060810
[    0.145005] Unable to detect cache hierarchy for CPU 0
[    0.145347] SCSI Media Changer driver v0.25
[    0.145846] Rockchip WiFi SYS interface (V1.00) ...
[    0.146238] ff400000.usb supply vusb_d not found, using dummy regulator
[    0.146327] ff400000.usb supply vusb_a not found, using dummy regulator
[    0.259055] dwc2 ff400000.usb: EPs: 10, dedicated fifos, 972 entries in SPRAM
[    0.259581] dwc2 ff400000.usb: DWC OTG Controller
[    0.259645] dwc2 ff400000.usb: new USB bus registered, assigned bus number 1
[    0.259698] dwc2 ff400000.usb: irq 20, io mem 0xff400000
[    0.260742] hub 1-0:1.0: USB hub found
[    0.260810] hub 1-0:1.0: 1 port detected
[    0.261689] ehci_hcd: USB 2.0 'Enhanced' Host Controller (EHCI) Driver
[    0.261724] ehci-platform: EHCI generic platform driver
[    0.261963] ohci_hcd: USB 1.1 'Open' Host Controller (OHCI) Driver
[    0.262035] ohci-platform: OHCI generic platform driver
[    0.262493] usbcore: registered new interface driver usb-storage
[    0.262639] usbcore: registered new interface driver usbserial
[    0.262699] usbcore: registered new interface driver cp210x
[    0.262755] usbserial: USB Serial support registered for cp210x
[    0.262822] usbcore: registered new interface driver pl2303
[    0.262867] usbserial: USB Serial support registered for pl2303
[    0.263393] i2c /dev entries driver
[    0.265685] rk_tsadcv2_temp_to_code: Invalid conversion table: code=4095, temperature=2147483647
[    0.265908] rockchip-thermal ff1f0000.tsadc: tsadc is probed successfully!
[    0.266304] Bluetooth: HCI UART driver ver 2.3
[    0.266328] Bluetooth: HCI UART protocol H4 registered
[    0.266339] Bluetooth: HCI UART protocol LL registered
[    0.266572] cpu cpu0: leakage=9
[    0.266768] cpu cpu0: Failed to get pvtm
[    0.267272] cpufreq: trying to register driver cpufreq-dt
[    0.268648] cpufreq: driver cpufreq-dt up and running
[    0.269247] Synopsys Designware Multimedia Card Interface Driver
[    0.270150] dwmmc_rockchip ff4a0000.dwmmc: num-slots property not found, assuming 1 slot is available
[    0.270275] dwmmc_rockchip ff4a0000.dwmmc: IDMAC supports 32-bit address mode.
[    0.270314] dwmmc_rockchip ff4a0000.dwmmc: Using internal DMA controller.
[    0.270342] dwmmc_rockchip ff4a0000.dwmmc: Version ID is 270a
[    0.270411] dwmmc_rockchip ff4a0000.dwmmc: DW MMC controller at irq 21,32 bit host data width,256 deep fifo
[    0.270491] dwmmc_rockchip ff4a0000.dwmmc: No vmmc regulator found
[    0.270506] dwmmc_rockchip ff4a0000.dwmmc: No vqmmc regulator found
[    0.270828] dwmmc_rockchip ff4a0000.dwmmc: allocated mmc-pwrseq
[    0.282167] mmc_host mmc0: Bus speed (slot 0) = 400000Hz (slot req 400000Hz, actual 400000HZ div = 0)
[    0.293180] dwmmc_rockchip ff4a0000.dwmmc: 1 slots initialized
[    0.293811] usbcore: registered new interface driver usbhid
[    0.293834] usbhid: USB HID core driver
[    0.295649] rknandc_base v1.1 2017-01-11
[    0.295970] rknandc ff4b0000.nandc: rknandc_probe clk rate = 147456000
[    0.296086] rkflash_dev_init
[    0.296104] init rkflash[0]
[    0.296142] SFTL version: 5.0.48 20180930
[    0.301191] dwmmc_rockchip ff4a0000.dwmmc: card claims to support voltages below defined range
[    0.311485] mmc_host mmc0: Bus speed (slot 0) = 50000000Hz (slot req 50000000Hz, actual 50000000HZ div = 0)
[    0.312636] mmc0: new high speed SDIO card at address 0001
[    0.330790] ...FtlVpcCheckAndModify enter...
[    0.345077] FtlCheckVpc 41 = 40  0
[    0.345098] FtlCheckVpc f5 = 40  0
[    0.346155] rkflash[0] init success
[    0.354597] rkflashd vendor storage init ok !
[    0.395283] Alternate GPT is invalid, using primary GPT.
[    0.395368]  rkflash0: p1 p2 p3 p4 p5 p6 p7 p8 p9
[    0.397637] rksfc_base v1.1 2016-01-08
[    0.398939] rk3308-acodec ff560000.acodec: Don't need hp-ctl gpio
[    0.399078] rk3308-acodec ff560000.acodec: De-pop as much as possible
[    0.451751] rk-multicodecs acodec-sound: rk3308-hifi <-> ff320000.i2s mapping ok
[    0.453148] input: rockchip,rk3308-acodec Headphones as /devices/platform/acodec-sound/sound/card0/input0
[    0.454567] NET: Registered protocol family 10
[    0.455606] NET: Registered protocol family 17
[    0.455670] NET: Registered protocol family 15
[    0.455909] Bluetooth: RFCOMM TTY layer initialized
[    0.455940] Bluetooth: RFCOMM socket layer initialized
[    0.455977] Bluetooth: RFCOMM ver 1.11
[    0.456031] Bluetooth: HIDP (Human Interface Emulation) ver 1.2
[    0.456055] Bluetooth: HIDP socket layer initialized
[    0.456071] [WLAN_Rhostname: can't open '/etc/hostname': No such file or directory
FKILL]: Enter rfkill_wlan_init
[    0.456310] [WLAN_RFKILL]: Enter rfkill_wlan_probe
[    0.456349] [WLAN_RFKILL]: wlan_platdata_parse_dt: wifi_chip_type = rtl8189fs
[    0.456359] [WLAN_RFKILL]: wlan_platdata_parse_dt: enable wifi power control.
[    0.456368] [WLAN_RFKILL]: wlan_platdata_parse_dt: wifi power controled by gpio.
[    0.456457] [WLAN_RFKILL]: wlan_platdata_parse_dt: get property: WIFI,host_wake_irq = 0, flags = 0.
[    0.456477] [WLAN_RFKILL]: wlan_platdata_parse_dt: The ref_wifi_clk not found !
[    0.456487] [WLAN_RFKILL]: rfkill_wlan_probe: init gpio
[    0.456498] [WLAN_RFKILL]: Exit rfkill_wlan_probe
[    0.456561] [BT_RFKILL]: Enter rfkill_rk_init
[    0.456911] flash vendor_init_thread!
[    0.456936] flash vendor storage:20170308 ret = -1
[    0.458694] input: adc-keys0 as /devices/platform/adc-keys0/input/input1
[    0.459885] input: gpio-keys as /devices/platform/gpio-keys/input/input2
[    0.460362] hctosys: unable to open rtc device (rtc0)
[    0.471756] vcc_sd: disabling
[    0.472217] ALSA device list:
[    0.472240]   #0: rockchip,rk3308-acodec
[    0.485293] VFS: Mounted root (squashfs filesystem) readonly on device 31:7.
[    0.504361] devtmpfs: mounted
[    0.504618] Freeing unused kernel memory: 320K
[    1.801747] random: nonblocking pool is initialized
modprobe: can't change directory to '/lib/modules': No such file or directory
dbus[184]: Unknown username "pulse" in message bus configuration file
ip: RTNETLINK answers: File exists
no valid interfaces found
W: [pulseaudio] main.c: Running in system mode, but --disallow-exit not set.
W: [pulseaudio] main.c: Running in system mode, but --disallow-module-loading not set.
N: [pulseaudio] main.c: Running in syst[em mode, forcibly disa bling SHM mode.
   3.462128] vendor storage:20160801 ret = -1
E: [pulseaudio] main.c: Daemon startup failed.
[    3.502269] file system registered
[    3.526219] read descriptors
[    3.526286] read strings
[    3.698073]
[    3.698114] =======================================================
[    3.698127] ==== Launching Wi-Fi driver! (Powered by Rockchip) ====
[    3.698135] =======================================================
[    3.698144] Realtek 8189FS SDIO WiFi driver (Powered by Rockchip,Ver v5.3.12_28613.20180703) init.
[    3.698160] [WLAN_RFKILL]: rockchip_wifi_power: 1
[    3.698171] [BT_RFKILL]: rfkill_get_bt_power_state: rfkill-bt driver has not Successful initialized
[    3.698181] [WLAN_RFKILL]: wifi turn on power. -1
[    3.698191] mmc0:mmc host rescan start!
[    3.698199] RTW: module init start
[    3.698209] RTW: rtl8189fs v5.3.12_28613.20180703
[    3.698217] RTW: build time: Jul  1 2019 12:07:48
[    3.698226] RTW: ## Calling platform_driver_register
[    4.524187] dwc2 ff400000.usb: bound driver configfs-gadget
[    4.698177] RTW: rtw_android_wifictrl_func_add: platform_driver_register timeout
[    4.698246] [WLAN_RFKILL]: rockchip_wifi_get_oob_irq: Enter
[    4.698359] RTW: rtw_inetaddr_notifier_register
[    4.698717] RTW: == SDIO Card Info ==
[    4.698758] RTW:   clock: 50000000 Hz
[    4.698778] RTW:   timing spec: sd high-speed
[    4.698810] RTW:   sd3_bus_mode: FALSE
[    4.698828] RTW: ================
[    4.698848] RTW: CHIP TYPE: RTL8188F
[    4.699328] RTW: rtw_hal_config_rftype RF_Type is 0 TotalTxPath is 1
[    4.699384] RTW: Chip Version Info: CHIP_8188F_Normal_Chip_SMIC_B_CUT_1T1R_RomVer(0)
[    4.699587] RTW: SetHwReg8188F: hci_sus_state=1
[    4.701557] RTW: SetHwReg: bMacPwrCtrlOn=1
[    4.701602] RTW: SetHwReg8188F: hci_sus_state=2
[    4.701921] RTW: sdio_power_on_check: val_mix:0x0000063f, res:0x0000063f
[    4.701957] RTW: sdio_power_on_check: 0x100 the result of cmd52 and cmd53 is the same.
[    4.702104] RTW: sdio_power_on_check: 0x1B8 test Pass.
[    4.702236] RTW: EEPROM type is E-FUSE
[    4.702655] RTW: hal_EfuseSwitchToBank: Efuse switch bank to 0
[    4.741037] RTW: hal_ReadEFuse_WiFi: data end at address=0xa0
[    4.741129] RTW: HW EFUSE
[    4.741146] RTW: 0x000: 29 81 03 CC  00 00 50 00  00 00 04 CC  0A 0C 00 00
[    4.741217] RTW: 0x010: 29 29 29 29  28 28 2A 2A  2A 2B 2B 02  FF FF FF FF
[    4.741284] RTW: 0x020: FF FF FF FF  FF FF FF FF  FF FF FF FF  FF FF FF FF
[    4.741352] RTW: 0x030: FF FF FF FF  FF FF FF FF  FF FF FF FF  FF FF FF FF
[    4.741420] RTW: 0x040: FF FF FF FF  FF FF FF FF  FF FF FF FF  FF FF FF FF
[    4.741487] RTW: 0x050: FF FF FF FF  FF FF FF FF  FF FF FF FF  FF FF FF FF
[    4.741555] RTW: 0x060: FF FF FF FF  FF FF FF FF  FF FF FF FF  FF FF FF FF
[    4.741626] RTW: 0x070: FF FF FF FF  FF FF FF FF  FF FF FF FF  FF FF FF FF
[    4.741693] RTW: 0x080: FF FF FF FF  FF FF FF FF  FF FF FF FF  FF FF FF FF
[    4.741760] RTW: 0x090: FF FF FF FF  FF FF FF FF  FF FF FF FF  FF FF FF FF
[    4.741828] RTW: 0x0A0: FF FF FF FF  FF FF FF FF  FF FF FF FF  FF FF FF FF
[    4.741895] RTW: 0x0B0: FF FF FF FF  FF FF FF FF  23 2F 20 00  00 00 00 FF
[    4.741962] RTW: 0x0C0: FF 02 00 10  00 FF 00 FF  00 00 FF FF  FF FF FF FF
[    4.742103] RTW: 0x0D0: 3E 10 01 12  23 FF FF FF  20 04 4C 02  79 F1 21 02
[    4.742177] RTW: 0x0E0: 0C 00 22 04  00 08 00 32  FF 21 02 0C  00 22 2A 01
[    4.742256] RTW: 0x0F0: 01 00 00 00  00 00 00 00  00 00 00 00  02 00 FF FF
[    4.742338] RTW: 0x100: 00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00
[    4.742418] RTW: 0x110: 00 EB 00 6E  01 00 00 00  00 FF 30 49  58 83 25 CD
[    4.742515] RTW: 0x120: FF FF FF FF  FF FF FF FF  FF FF FF FF  FF FF FF FF
[    4.742597] RTW: 0x130: FF FF FF FF  FF FF FF FF  FF FF FF FF  FF FF FF FF
[    4.742683] RTW: 0x140: FF FF FF FF  FF FF FF FF  FF FF FF FF  FF FF FF FF
[    4.742761] RTW: 0x150: FF FF FF FF  FF FF FF FF  FF FF FF FF  FF FF FF FF
[    4.742831] RTW: 0x160: FF FF FF FF  FF FF FF FF  FF FF FF FF  FF FF FF FF
[    4.742898] RTW: 0x170: FF FF FF FF  FF FF FF FF  FF FF FF FF  FF FF FF FF
[    4.742966] RTW: 0x180: FF FF FF FF  FF FF FF FF  FF FF FF FF  FF FF FF FF
[    4.743085] RTW: 0x190: FF FF FF FF  FF FF FF FF  FF FF FF FF  FF FF FF FF
[    4.743162] RTW: 0x1A0: FF FF FF FF  FF FF FF FF  FF FF FF FF  FF FF FF FF
[    4.743249] RTW: 0x1B0: FF FF FF FF  FF FF FF FF  FF FF FF FF  FF FF FF FF
[    4.743321] RTW: 0x1C0: FF FF FF FF  FF FF FF FF  FF FF FF FF  FF FF FF FF
[    4.743390] RTW: 0x1D0: FF FF FF FF  FF FF FF FF  FF FF FF FF  FF FF FF FF
[    4.743462] RTW: 0x1E0: FF FF FF FF  FF FF FF FF  FF FF FF FF  FF FF FF FF
[    4.743529] RTW: 0x1F0: FF FF FF FF  FF FF FF FF  FF FF FF FF  FF FF FF FF
[    4.743619] RTW: hal_com_config_channel_plan chplan:0x23
[    4.743630] RTW: Hal_DetectWoWMode
[    4.744142] RTW: kfree Pwr Trim flag:1
[    4.744160] RTW: bb_gain:-2
[    4.744268] RTW: rtl8188f_FirmwareDownload((null)) tmp_ps=3
[    4.744280] RTW: rtl8188f_FirmwareDownload fw: FW_NIC, size: 20306
[    4.744299] RTW: rtl8188f_FirmwareDownload: fw_ver=e fw_subver=0000 sig=0x88f1, Month=06, Date=07, Hour=17, Minute=18
[    4.744317] RTW: rtl8188f_FirmwareDownload(): Shift for fw header!
[    4.744326] RTW: rtl8188f_FirmwareDownload by IO write!
[    4.823383] RTW: polling_fwdl_chksum: Checksum report OK! (1, 0ms), REG_MCUFWDL:0x07040105
[    4.823735] RTW: _8051Reset8188: Finish
[    4.837290] RTW: _FWFreeToGo: Polling FW ready OK! (187, 14ms), REG_MCUFWDL:0x070401c6
[    4.837311] RTW: rtl8188f_FirmwareDownload: DLFW OK !
[    4.837321] RTW: rtl8188f_FirmwareDownload success. write_fw:1, 93ms
[    4.837357] RTW:  <=== rtl8188f_FirmwareDownload()
[    4.848795] RTW: hal_read_mac_hidden_rpt OK! (2, 11ms), fwdl:1, id:0x19
[    4.849267] RTW: SetHwReg: bMacPwrCtrlOn=0
[    4.849288] RTW: SetHwReg8188F: hci_sus_state=3
[    4.849856] RTW: SetHwReg8188F: hci_sus_state=0
[    4.849871] RTW: rtw_hal_read_chip_info in 150 ms
[    4.849908] RTW: init_channel_set((null)) ChannelPlan ID:0x23, ch num:14
[    4.850841] RTW: rtw_alloc_macid((null)) if1, mac_addr:ff:ff:ff:ff:ff:ff macid:1
[    4.851766] RTW: rtw_init_pwrctrl_priv: set GPIO_0 1 as default.
[    4.851812] RTW: ADAPTIVITY_VERSION 9.5.7
[    4.851821] RTW: RTW_ADAPTIVITY_EN_ENABLE
[    4.851832] RTW: RTW_ADAPTIVITY_MODE_NORMAL
[    4.851842] RTW: RTW_ADAPTIVITY_DML_DISABLE
[    4.851852] RTW: RTW_ADAPTIVITY_DC_BACKOFF:2
[    4.851861] RTW: IQK FW offload:disable
[    4.851874] RTW: Init_ODM_ComInfo_8188f(): fab_ver=0 cut_ver=12
[    4.851889] RTW: rtw_regsty_chk_target_tx_power_valid return _FALSE for band:0, path:0, rs:0, t:-1
[    4.852537] RTW: retriveFromFile openFile path:/userdata/cfg/init.d/PHY_REG_PG.txt fp=ffffffc00ef1b900
[    4.852572] RTW: retriveFromFile readFile, ret:656
[    4.854091] RTW: retriveFromFile openFile path:/userdata/cfg/init.d/TXPWR_LMT.txt fp=ffffffc00efb0500
[    4.854125] RTW: retriveFromFile readFile, ret:3012
[    4.854154] RTW: phy_ParsePowerLimitTableFile enter
[    4.854604] RTW: phy_ParsePowerLimitTableFile return 1
[    4.854629] RTW: default mapping domain:0x23 to regd_name:MKK
[    4.854647] RTW: rtw_macaddr_cfg mac addr:30:49:58:83:25:cd
[    4.854771] RTW: bDriverStopped:True, bSurpriseRemoved:False, bup:0, hw_init_completed:0
[    4.855744] RTW: rtw_alloc_macid((null)) if2, mac_addr:ff:ff:ff:ff:ff:ff macid:1
[    4.855792] RTW: rtw_drv_add_vir_if if2 mac_addr : 32:49:58:83:25:cd
[    4.855876] RTW: rtw_wiphy_alloc(phy0)
[    4.855888] RTW: rtw_wdev_alloc(padapter=ffffff8008976000)
[    4.855920] RTW: rtw_wiphy_alloc(phy1)
[    4.855929] RTW: rtw_wdev_alloc(padapter=ffffff8008ad9000)
[    4.855942] RTW: rtw_wiphy_register(phy0)
[    4.855951] RTW: Register RTW cfg80211 vendor cmd(0x67) interface
[    4.856246] RTW: rtw_reg_notifier: NL80211_REGDOM_SET_BY_CORE
[    4.856629] RTW: rtw_ndev_init(wlan0) if1 mac_addr=30:49:58:83:25:cd
[    4.857157] RTW: rtw_ndev_notifier_call(wlan0) state:16
[    4.859134] RTW: rtw_ndev_notifier_call(wlan0) state:5
[    4.860818] RTW: cfg80211_rtw_get_txpower
[    4.862699] RTW: rtw_wiphy_register(phy1)
[    4.862857] RTW: Register RTW cfg80211 vendor cmd(0x67) interface
[    4.863567] RTW: rtw_reg_notifier: NL80211_REGDOM_SET_BY_CORE
[    4.864848] RTW: rtw_ndev_init(p2p0) if2 mac_addr=32:49:58:83:25:cd
[    4.865985] RTW: rtw_ndev_notifier_call(p2p0) state:16
[    4.871768] RTW: rtw_ndev_notifier_call(p2p0) state:5
[    4.873126] RTW: gpio_hostwakeup_alloc_irq : oob_irq = 30
[    4.873385] RTW: allocate gpio irq 30 ok
[    4.873920] RTW: module init ret=0
[    4.961802] RTW: rtw_ndev_notifier_call(wlan0) state:13
[    4.961848] RTW: _netdev_open(wlan0) , bup=0
[    4.962083] RTW: FW does not exist before power on!!
[    4.962660] RTW: SetHwReg8188F: hci_sus_state=1
[    4.964385] RTW: SetHwReg: bMacPwrCtrlOn=1
[    4.964414] RTW: SetHwReg8188F: hci_sus_state=2
[    4.964607] RTW: sdio_power_on_check: val_mix:0x0000063f, res:0x0000063f
[    4.964623] RTW: sdio_power_on_check: 0x100 the result of cmd52 and cmd53 is the same.
[    4.964681] RTW: sdio_power_on_check: 0x1B8 test Pass.
[    4.964696] RTW: Power on ok!
[    4.964846] RTW: rtl8188f_FirmwareDownload(wlan0) tmp_ps=3
[    4.964862] RTW: rtl8188f_FirmwareDownload fw: FW_NIC, size: 20306
[    4.964877] RTW: rtl8188f_FirmwareDownload: fw_ver=e fw_subver=0000 sig=0x88f1, Month=06, Date=07, Hour=17, Minute=18
[    4.964886] RTW: rtl8188f_FirmwareDownload(): Shift for fw header!
[    4.964894] RTW: rtl8188f_FirmwareDownload by IO write!
[    5.046159] RTW: polling_fwdl_chksum: Checksum report OK! (1, 0ms), REG_MCUFWDL:0x00040105
[    5.046510] RTW: _8051Reset8188: Finish
[  Playing WAVE '/usr/lib/silence.wav'  : Signed 16 bit  Little Endian, Rate 48000 Hz, Stereo
5.060066] RTW: _FWFreeToGo: Polling FW ready OK! (197, 14ms), REG_MCUFWDL:0x000401c6
[    5.060091] RTW: rtl8188f_FirmwareDownload: DLFW OK !
[    5.060101] RTW: rtl8188f_FirmwareDownload success. write_fw:1, 96ms
[    5.060136] RTW:  <=== rtl8188f_FirmwareDownload()
[    5.060151] RTW: HalDetectPwrDownMode(): PDN=0
[    5.060159] RTW: Set RF Chip ID to RF_6052 and RF type to 0.
[    5.369182] RTW: rtw_hal_set_macaddr_port wlan0- hw port(0) mac_addr =30:49:58:83:25:cd
[    5.369330] RTW: rtw_hal_set_macaddr_port p2p0- hw port(1) mac_addr =32:49:58:83:25:cd
[    5.369569] RTW: rtw_hal_get_macaddr_port wlan0- hw port(0) mac_addr =30:49:58:83:25:cd
[    5.369588] RTW: wlan0- hw port(0) mac_addr =30:49:58:83:25:cd
[    5.369712] RTW: rtw_hal_get_macaddr_port p2p0- hw port(1) mac_addr =32:49:58:83:25:cd
[    5.369729] RTW: p2p0- hw port(1) mac_addr =32:49:58:83:25:cd
[    5.369855] RTW: [HW_VAR_ENABLE_RX_BAR] 0x6A2=0x500
[    5.371702] RTW: rtw_rf_get_kfree_tx_gain_offset path:0, ch:6, bb_gain_sel:0, kfree_offset:-2
[    5.372019] RTW: kfree gain_offset 0x55:0x82060 RTW:  after :0xa060
[    5.372616] RTW: MAC Address = 30:49:58:83:25:cd
[    5.372628] RTW: rtw_start_drv_threads(wlan0) start RTW_XMIT_THREAD
[    5.372782] RTW: rtw_start_drv_threads(wlan0) start RTW_CMD_THREAD
[    5.372912] RTW: rtl8188f_start_thread(wlan0) start RTWHALXT
[    5.373070] RTW: start rtl8188fs_xmit_thread(wlan0)
[    5.373271] RTW: rtw_cfg80211_init_wiphy:rf_type=0
[    5.373298] RTW: [HT] HAL Support STBC = 0x01
[    5.373320] RTW: _netdev_vir_if_open(p2p0) , bup=0
[    5.373338] RTW: rtl8188f_start_thread(p2p0) start RTWHALXT
[    5.373449] RTW: rtw_cfg80211_init_wiphy:rf_type=0
[    5.373470] RTW: start rtl8188fs_xmit_thread(p2p0)
[    5.373566] RTW: [HT] HAL Support STBC = 0x01
[    5.373588] RTW: _netdev_vir_if_open(p2p0) (bup=1) exit
[    5.373598] RTW: -871x_drv - drv_open, bup=1
[    5.373702] RTW: cfg80211_rtw_set_power_mgmt(wlan0) enabled:1, timeout:-1
[    5.373731] IPv6: ADDRCONF(NETDEV_UP): wlan0: link is not ready
[    5.373744] RTW: rtw_ndev_notifier_call(wlan0) state:1
[    5.374708] RTW: cfg80211_rtw_get_txpower
[    5.409220] RTW: rtw_ndev_notifier_call(p2p0) state:13
[    5.409259] RTW: _netdev_vir_if_open(p2p0) , bup=1
[    5.409274] RTW: rtw_cfg80211_init_wiphy:rf_type=0
[    5.409286] RTW: [HT] HAL Support STBC = 0x01
[    5.409307] RTW: _netdev_vir_if_open(p2p0) (bup=1) exit
[    5.409446] RTW: cfg80211_rtw_set_power_mgmt(p2p0) enabled:1, timeout:-1
[    5.409488] IPv6: ADDRCONF(NETDEV_UP): p2p0: link is not ready
[    5.409502] RTW: rtw_ndev_notifier_call(p2p0) state:1
play WARN alsa: can't encode 0-bit Unknown or not applicable
[    7.379638] RTW: nolinked power save enter
[   11.957654] Current WiFi chip is RTL8189FS.
killall: hostapd: no process killed
[   12.643278] RTW: wlan0- hw port(0) mac_addr =30:49:58:83:25:cd
[   12.643437] RTW: p2p0- hw port(1) mac_addr =32:49:58:83:25:cd
[   12.646123] RTW: nolinked power save leave
rm: can't remove '/tmp/music': No such file or directory
killall: cpm: no process killed
killall: onboard_ui: no process killed
killall: carrier: no process killed
killall: charge_task: no process killed
killall: clean_task: no process killed
killall: config_server: no process killed
killall: debug_proxy: no process killed
killall: event_hub: no process killed
killall: av_task: no process killed
killall: find_charger_task: no process killed
killall: remote_control_task: no process killed
killall: idle_task: no process killed
killall: navigator: no process killed
killall: shared_memory: no process killed
killall: slam_pose_provider: no process killed
killall: task_manager: no process killed
killall: config_node: no process killed
killall: network_proxy: no process killed
killall: time_server_tactics: no process killed
killall: updater: no process killed
killall: ledflash.sh: no process killed
kill: can't kill pid 429: No such process
killall: data_collect: no process killed
[   13.897212] sh (383): drop_caches: 1
/etc/init.d/S98_lunch_init: source: line 91: can't open '/data/cfg/rockchip_test/auto_reboot.sh'
input-event-daemon: Start listening on 3 devices...
eufy-RoboVac login: [   14.308152] RTW: nolinked power save enter
[   14.533091] of_dma_request_slave_channel: dma-names property of node '/serial@ff0b0000' missing or empty
[   14.533137] ttyS1 - failed to request DMA, use interrupt mode
[   14.749761] RTW: wlan0- hw port(0) mac_addr =30:49:58:83:25:cd
[   14.749911] RTW: p2p0- hw port(1) mac_addr =32:49:58:83:25:cd
[   14.752591] RTW: nolinked power save leave
[   14.752767] RTW: rtw_set_802_11_connect(wlan0)  fw_state=0x00000000
[   15.103947] RTW: start auth
[   15.108841] RTW: auth success, start assoc
[   15.111259] RTW: assoc success
[   15.111554] IPv6: ADDRCONF(NETDEV_CHANGE): wlan0: link becomes ready
[   15.114641] RTW: recv eapol packet
[   15.116256] RTW: ============ STA [1c:3b:f3:a8:7c:cc]  ===================
[   15.116307] RTW: mac_id : 0
[   15.116341] RTW: wireless_mode : 0x0a
[   15.116361] RTW: mimo_type : 0
[   15.116383] RTW: bw_mode : 20MHz, ra_bw_mode : 20MHz
[   15.116401] RTW: rate_id : 5
[   15.116421] RTW: rssi : 28 (%), rssi_level : 0
[   15.116441] RTW: is_support_sgi : Y, is_vht_enable : N
[   15.116461] RTW: disable_ra : N, disable_pt : N
[   15.116480] RTW: is_noisy : N
[   15.116498] RTW: txrx_state : 0
[   15.116519] RTW: curr_tx_rate : CCK_1M (L)
[   15.116546] RTW: curr_tx_bw : 20MHz
[   15.116565] RTW: curr_retry_ratio : 0
[   15.116584] RTW: ra_mask : 0x00000000000ffff0
[   15.116584]
[   15.119642] RTW: send eapol packet
[   15.159702] RTW: recv eapol packet
[   15.161205] RTW: send eapol packet
[   15.162436] RTW: set pairwise key camid:0, addr:1c:3b:f3:a8:7c:cc, kid:0, type:AES
[   15.163459] RTW: set group key camid:1, addr:1c:3b:f3:a8:7c:cc, kid:1, type:AES

Login timed out after 60 seconds
eufy-RoboVac login:
```
