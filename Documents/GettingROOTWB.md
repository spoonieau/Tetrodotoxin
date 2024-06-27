# Getting ROOT - Wifi Board
- The firmware on the L70 is Linux with DropbearSSH and ADB as services, but the default is to have these service turned off.
- Get the following tools.   
```
$ sudo pacman -S dropbear android-udev android-tools
```
- The init scripts are looking to see if a file is present in the userdata partition, if present the service starts.
- Mount the userdata image dumped previously [Dumping l70 firmware](https://github.com/spoonieau/Tetrodotoxin/blob/main/Documents/DumpingFirmwareWB.md "Dumping L70 firmware")  
```
$ sudo mkdir /mnt/eufy
$ sudo mount <location to image>/userdata.img /mnt/eufy
$ cd /mnt/eufy
$ sudo touch /cfg/init.d/adbd
$ sudo touch /cfg/init.d/dropbear
$ cd /
$ sudo umount 
```
- Using the same process as in [Dumping l70 firmware](https://github.com/spoonieau/Tetrodotoxin/blob/main/Documents/DumpingFirmwareWB.md "Dumping L70 firmware") reconnect to the L70 in Gaget mode.
- Using the 'update_tool' flash the modfied userdata.img back to the device.
```
./upgrade_tool WL 0x00029800 userdata.img
```
-When writing is complete, unpulg the micro usb cable to power off the device.    
-Reconnect the micro usb cable to the L70 debug port the L70 will boot up like normal, lsusb should report something simmilar.  
```
$ lsusb
Bus 001 Device 011: ID 2207:0006 Fuzhou Rockchip Electronics Company rk3xxx
```
- ADB devices will report
```
$ adb devices
0123456789ABCDEF        device
```
- Start ADB Shell and reset the root password.
``` 
$ adb shell
/ # ls
bin            lib64          oem            run            userdata
data           linuxrc        opt            sbin           usr
dev            media          proc           sys            var
etc            misc           rockchip_test  system
lib            mnt            root           tmp
/ # passwd
Changing password for root
New password:
Retype password: 
passwd: password for root changed by root
/ # exit
```
- Disconnect micro USB and hold down the power button to turn L70 off, then hold again to power back up.
- Device is now able to be logged in with root via ssh. Get the L70 wifi IP from your routers DHCP lease.
```
$ dbclient root@XXX.XXX.XXX.XXX <- replace with the device IP
Host 'XXX.XXX.XXX.XXX' is not in the trusted hosts file.
(ecdsa-sha2-nistp521 fingerprint SHA256:L43DPgajVd2vtFctaiGCCn4qqYRrKyfs2gun6BMFEoc)
Do you want to continue connecting? (y/n) y
root@xxx.xxx.xxx.xxx's password: 
[root@eufy-RoboVac:~]#
```
- Congratulations the L70 is now yours...

- Some interesting info from the L70.   
```
[root@eufy-RoboVac:~]# uname -a
Linux eufy-RoboVac 4.4.143 #54 SMP PREEMPT Sat Nov 2 15:27:01 CST 2019 aarch64 GNU/Linux
```

```
[root@eufy-RoboVac:~]# cat /proc/cpuinfo
processor       : 0
BogoMIPS        : 48.00
Features        : fp asimd aes pmull sha1 sha2 crc32
CPU implementer : 0x41
CPU architecture: 8
CPU variant     : 0x0
CPU part        : 0xd04
CPU revision    : 2

processor       : 1
BogoMIPS        : 48.00
Features        : fp asimd aes pmull sha1 sha2 crc32
CPU implementer : 0x41
CPU architecture: 8
CPU variant     : 0x0
CPU part        : 0xd04
CPU revision    : 2

processor       : 2
BogoMIPS        : 48.00
Features        : fp asimd aes pmull sha1 sha2 crc32
CPU implementer : 0x41
CPU architecture: 8
CPU variant     : 0x0
CPU part        : 0xd04
CPU revision    : 2

processor       : 3
BogoMIPS        : 48.00
Features        : fp asimd aes pmull sha1 sha2 crc32
CPU implementer : 0x41
CPU architecture: 8
CPU variant     : 0x0
CPU part        : 0xd04
CPU revision    : 2

Serial          : XXXXXXXXXXXXXXXX
```

```
[root@eufy-RoboVac:~]# ps aux
    1 root      2404 S    init
    2 root         0 SW   [kthreadd]
    3 root         0 SW   [ksoftirqd/0]
    4 root         0 SW   [kworker/0:0]
    5 root         0 SW<  [kworker/0:0H]
    7 root         0 SW   [rcu_preempt]
    8 root         0 SW   [rcu_sched]
    9 root         0 SW   [rcu_bh]
   10 root         0 SW   [migration/0]
   11 root         0 SW   [watchdog/0]
   12 root         0 SW   [watchdog/1]
   13 root         0 SW   [migration/1]
   14 root         0 SW   [ksoftirqd/1]
   15 root         0 SW   [kworker/1:0]
   16 root         0 SW<  [kworker/1:0H]
   17 root         0 SW   [watchdog/2]
   18 root         0 SW   [migration/2]
   19 root         0 SW   [ksoftirqd/2]
   20 root         0 SW   [kworker/2:0]
   21 root         0 SW<  [kworker/2:0H]
   22 root         0 SW   [watchdog/3]
   23 root         0 SW   [migration/3]
   24 root         0 SW   [ksoftirqd/3]
   26 root         0 SW<  [kworker/3:0H]
   27 root         0 SW   [kdevtmpfs]
   28 root         0 SW<  [perf]
   29 root         0 SW   [kconsole]
   30 root         0 SW   [khungtaskd]
   31 root         0 SW<  [writeback]
   32 root         0 SW<  [crypto]
   33 root         0 SW<  [bioset]
   34 root         0 SW<  [kblockd]
   35 root         0 SW<  [devfreq_wq]
   36 root         0 SW   [kworker/0:1]
   37 root         0 SW<  [cfg80211]
   38 root         0 SW   [cfinteractive]
   65 root         0 SW   [kswapd0]
   66 root         0 SW<  [vmstat]
   67 root         0 SW   [fsnotify_mark]
   68 root         0 SW<  [SquashFS read w]
   89 root         0 SW   [irq/191-rockchi]
   90 root         0 SW   [irq/192-rockchi]
   91 root         0 SW   [irq/193-rockchi]
   92 root         0 SW   [kworker/1:1]
   93 root         0 SW<  [dwc2]
   94 root         0 SW   [irq/14-rockchip]
   95 root         0 SW<  [bioset]
   96 root         0 DW   [rkflash]
   97 root         0 SW   [kworker/u8:2]
   98 root         0 SW<  [ipv6_addrconf]
   99 root         0 SW<  [krfcommd]
  102 root         0 SW<  [deferwq]
  103 root         0 SW   [kworker/2:1]
  105 root         0 SW   [kworker/3:1]
  109 root         0 SW<  [kworker/1:1H]
  111 root         0 SW<  [kworker/2:1H]
  122 root      2404 S    /sbin/syslogd -n
  125 root      2404 S    /sbin/klogd -n
  127 root      1920 S    /usr/bin/ueventd
  129 root         0 SW<  [kworker/0:1H]
  154 root         0 SW<  [kworker/3:1H]
  185 dbus      2716 S    dbus-daemon --system
  199 root      2128 S    /sbin/dhcpcd -f /etc/dhcpcd.conf
  202 root         0 SW   [kworker/3:3]
  205 root     72196 S    /usr/sbin/ntpd -g
  213 root      2316 S    /usr/sbin/dropbear -R
  230 root      218m S    adbd
  274 root         0 SW   [ksdioirqd/mmc0]
  287 root         0 SW   [RTW_XMIT_THREAD]
  288 root         0 SW   [RTW_CMD_THREAD]
  289 root         0 RW   [RTWHALXT]
  290 root         0 SW   [RTWHALXT]
  339 root      4440 S    wpa_supplicant -B -i wlan0 -c /data/cfg/wpa_supplica
  341 root      2404 S    sh /data/bin/dhcpcd_daemon
  433 root      232m S    ./cpm
  434 root      2404 S    {ledflash.sh} /bin/sh /usr/sbin/ledflash.sh fast
  440 root      1768 S    input-event-daemon -v
  451 root      232m S    config_node
  452 root      232m S    event_hub
  470 root      392m S    onboard_ui
  471 root      419m S    slam_pose_provider
  478 root      257m S    navigator
  486 root      528m S    carrier
  494 root      307m S    task_manager
  495 root      376m S    time_server_tactics
  500 root      921m S    network_proxy
  544 root      232m S    idle_task
  971 root         0 SW   [kworker/u8:3]
 1780 root      2672 R    /usr/sbin/dropbear -R
 1906 root      2404 S    -sh
 4513 root      2404 S    -/bin/login
 4663 root         0 SW   [kworker/u8:0]
 4911 root      2272 S    sleep 2
 4942 root      2272 S    sleep 0.2
 4943 root      2404 R    ps aux
```
```
[root@eufy-RoboVac:/bin]# busybox --help
BusyBox v1.27.2 (2019-07-01 14:43:08 CST) multi-call binary.
BusyBox is copyrighted by many authors between 1998-2015.
Licensed under GPLv2. See source distribution for detailed
copyright notices.

Usage: busybox [function [arguments]...]
   or: busybox --list[-full]
   or: busybox --install [-s] [DIR]
   or: function [arguments]...

        BusyBox is a multi-call binary that combines many common Unix
        utilities into a single executable.  Most people will create a
        link to busybox for each function they wish to use and BusyBox
        will act like whatever it was invoked as.

Currently defined functions:
        [, [[, ar, arp, arping, ash, awk, basename, blkid, bunzip2, bzcat, cat, chattr, chgrp, chmod, chown, chroot, chrt, chvt, cksum, clear, cmp, cp, cpio, crond, crontab, cut, date, dc, dd, deallocvt, devmem, df, diff, dirname, dmesg, dnsd,
        dnsdomainname, dos2unix, du, dumpkmap, echo, egrep, eject, env, ether-wake, expr, factor, fallocate, false, fbset, fdflush, fdformat, fdisk, fgrep, find, flock, fold, free, freeramdisk, fsck, fsfreeze, fstrim, fuser, getopt, getty, grep, gunzip,
        gzip, halt, hdparm, head, hexdump, hostid, hostname, hwclock, i2cdetect, i2cdump, i2cget, i2cset, id, ifconfig, ifdown, ifup, inetd, init, insmod, install, ip, ipaddr, ipcrm, ipcs, iplink, ipneigh, iproute, iprule, iptunnel, kill, killall, killall5,
        klogd, last, less, link, linux32, linux64, linuxrc, ln, loadfont, loadkmap, logger, login, logname, losetup, ls, lsattr, lsmod, lsof, lspci, lsscsi, lsusb, lzcat, lzma, makedevs, md5sum, mdev, mesg, microcom, mkdir, mkdosfs, mke2fs, mkfifo, mknod,
        mkswap, mktemp, modprobe, more, mount, mountpoint, mt, mv, nameif, netstat, nice, nl, nohup, nproc, nslookup, od, openvt, partprobe, passwd, paste, patch, pidof, ping, pipe_progress, pivot_root, poweroff, printenv, printf, ps, pwd, rdate, readlink,
        readprofile, realpath, reboot, renice, reset, resize, rm, rmdir, rmmod, route, run-parts, runlevel, sed, seq, setarch, setconsole, setkeycodes, setlogcons, setpriv, setserial, setsid, sh, sha1sum, sha256sum, sha3sum, sha512sum, shred, sleep, sort,
        ssl_client, start-stop-daemon, strings, stty, su, sulogin, svc, swapoff, swapon, switch_root, sync, sysctl, syslogd, tail, tar, taskset, tee, telnet, test, tftp, time, top, touch, tr, traceroute, true, truncate, tty, ubirename, udhcpc, uevent,
        umount, uname, uniq, unix2dos, unlink, unlzma, unxz, unzip, uptime, usleep, uudecode, uuencode, vconfig, vi, w, watch, watchdog, wc, wget, which, who, whoami, xargs, xxd, xz, xzcat, yes, zcat
```
```
[root@eufy-RoboVac:/]# free -m
             total       used       free     shared    buffers     cached
Mem:        246456      81372     165084        688       4536      19648
-/+ buffers/cache:      57188     189268
Swap:            0          0          0
```
```
[root@eufy-RoboVac:/]# df
Filesystem           1K-blocks      Used Available Use% Mounted on
/dev/root                23040     23040         0 100% /
devtmpfs                123068         0    123068   0% /dev
tmpfs                   123228         0    123228   0% /dev/shm
tmpfs                   123228       564    122664   0% /tmp
tmpfs                   123228        36    123192   0% /run
/dev/block/by-name/oem
                         20434     14440      4972  74% /oem
/dev/block/by-name/userdata
                         25232      2897     21072  12% /userdata
/dev/block/by-name/sysdata
                          1989       115      1774   6% /oem/bin/sys_data
```








     
  
       
