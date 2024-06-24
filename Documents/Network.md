 
# Network

## After Factory Reset

- Unit will create a AP With the SSID of ```eufy RoboVac L70 Hybrid-abcd``` with no password.
- When device is in AP mode it has its own DHCP Server.
- Device AP mode IP Address ```192.168.78.1```
### Nmap TCP Intense Scan Results
```
nmap -p 1-65535 -T4 -A -v 192.168.78.1
Starting Nmap 7.95 ( https://nmap.org ) at 2024-05-16 15:11 AWST
NSE: Loaded 157 scripts for scanning.
NSE: Script Pre-scanning.
Initiating NSE at 15:11
Completed NSE at 15:11, 0.00s elapsed
Initiating NSE at 15:11
Completed NSE at 15:11, 0.00s elapsed
Initiating NSE at 15:11
Completed NSE at 15:11, 0.00s elapsed
Initiating ARP Ping Scan at 15:11
Scanning 192.168.78.1 [1 port]
Completed ARP Ping Scan at 15:11, 0.11s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 15:11
Completed Parallel DNS resolution of 1 host. at 15:11, 13.00s elapsed
Initiating SYN Stealth Scan at 15:11
Scanning 192.168.78.1 [65535 ports]
Discovered open port 53/tcp on 192.168.78.1
Completed SYN Stealth Scan at 15:12, 12.08s elapsed (65535 total ports)
Initiating Service scan at 15:12
Scanning 1 service on 192.168.78.1
Completed Service scan at 15:12, 6.07s elapsed (1 service on 1 host)
Initiating OS detection (try #1) against 192.168.78.1
NSE: Script scanning 192.168.78.1.
Initiating NSE at 15:12
Completed NSE at 15:12, 8.24s elapsed
Initiating NSE at 15:12
Completed NSE at 15:12, 0.00s elapsed
Initiating NSE at 15:12
Completed NSE at 15:12, 0.00s elapsed
Nmap scan report for 192.168.78.1
Host is up (0.0092s latency).
Not shown: 65534 closed tcp ports (reset)
PORT   STATE SERVICE VERSION
53/tcp open  domain  dnsmasq 2.78
| dns-nsid:
|_  bind.version: dnsmasq-2.78
MAC Address: 32:49:58:83:25:CD (Unknown)
Device type: general purpose
Running: Linux 3.X|4.X
OS CPE: cpe:/o:linux:linux_kernel:3 cpe:/o:linux:linux_kernel:4
OS details: Linux 3.2 - 4.14
Uptime guess: 0.039 days (since Thu May 16 14:15:48 2024)
Network Distance: 1 hop
TCP Sequence Prediction: Difficulty=257 (Good luck!)
IP ID Sequence Generation: All zeros

TRACEROUTE
HOP RTT     ADDRESS
1   9.17 ms 192.168.78.1

NSE: Script Post-scanning.
Initiating NSE at 15:12
Completed NSE at 15:12, 0.00s elapsed
Initiating NSE at 15:12
Completed NSE at 15:12, 0.00s elapsed
Initiating NSE at 15:12
Completed NSE at 15:12, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 40.89 seconds
           Raw packets sent: 67181 (2.957MB) | Rcvd: 65655 (2.627MB)
```
### Nmap UDP Intense Scan Results
```
nmap -sS -sU -T4 -A -v 192.168.78.1
Starting Nmap 7.95 ( https://nmap.org ) at 2024-05-16 14:25 AWST
NSE: Loaded 157 scripts for scanning.
NSE: Script Pre-scanning.
Initiating NSE at 14:25
Completed NSE at 14:25, 0.00s elapsed
Initiating NSE at 14:25
Completed NSE at 14:25, 0.00s elapsed
Initiating NSE at 14:25
Completed NSE at 14:25, 0.00s elapsed
Initiating ARP Ping Scan at 14:25
Scanning 192.168.78.1 [1 port]
Completed ARP Ping Scan at 14:25, 0.09s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 14:25
Completed Parallel DNS resolution of 1 host. at 14:25, 13.00s elapsed
Initiating SYN Stealth Scan at 14:25
Scanning 192.168.78.1 [1000 ports]
Discovered open port 53/tcp on 192.168.78.1
Completed SYN Stealth Scan at 14:25, 1.73s elapsed (1000 total ports)
Initiating UDP Scan at 14:25
Scanning 192.168.78.1 [1000 ports]
Increasing send delay for 192.168.78.1 from 0 to 50 due to max_successful_tryno increase to 5
Increasing send delay for 192.168.78.1 from 50 to 100 due to max_successful_tryno increase to 6
Warning: 192.168.78.1 giving up on port because retransmission cap hit (6).
Increasing send delay for 192.168.78.1 from 100 to 200 due to 11 out of 11 dropped probes since last increase.
UDP Scan Timing: About 6.46% done; ETC: 14:33 (0:07:29 remaining)
Increasing send delay for 192.168.78.1 from 200 to 400 due to 11 out of 13 dropped probes since last increase.
Increasing send delay for 192.168.78.1 from 400 to 800 due to 11 out of 13 dropped probes since last increase.
UDP Scan Timing: About 9.36% done; ETC: 14:36 (0:09:51 remaining)
UDP Scan Timing: About 12.43% done; ETC: 14:37 (0:10:41 remaining)
UDP Scan Timing: About 15.46% done; ETC: 14:38 (0:11:18 remaining)
UDP Scan Timing: About 29.36% done; ETC: 14:40 (0:10:38 remaining)
UDP Scan Timing: About 35.86% done; ETC: 14:40 (0:09:52 remaining)
UDP Scan Timing: About 41.69% done; ETC: 14:41 (0:09:03 remaining)
UDP Scan Timing: About 47.49% done; ETC: 14:41 (0:08:15 remaining)
UDP Scan Timing: About 53.13% done; ETC: 14:41 (0:07:26 remaining)
UDP Scan Timing: About 58.49% done; ETC: 14:41 (0:06:37 remaining)
UDP Scan Timing: About 63.84% done; ETC: 14:41 (0:05:47 remaining)
UDP Scan Timing: About 69.16% done; ETC: 14:41 (0:04:59 remaining)
Discovered open port 67/udp on 192.168.78.1
UDP Scan Timing: About 74.51% done; ETC: 14:41 (0:04:08 remaining)
UDP Scan Timing: About 79.64% done; ETC: 14:41 (0:03:18 remaining)
Discovered open port 123/udp on 192.168.78.1
UDP Scan Timing: About 84.64% done; ETC: 14:41 (0:02:29 remaining)
UDP Scan Timing: About 90.00% done; ETC: 14:41 (0:01:37 remaining)
Discovered open port 53/udp on 192.168.78.1
UDP Scan Timing: About 95.11% done; ETC: 14:41 (0:00:48 remaining)
Completed UDP Scan at 14:42, 1022.18s elapsed (1000 total ports)
Initiating Service scan at 14:42
Scanning 17 services on 192.168.78.1
Service scan Timing: About 21.05% done; ETC: 14:46 (0:03:08 remaining)
Completed Service scan at 14:44, 102.59s elapsed (19 services on 1 host)
Initiating OS detection (try #1) against 192.168.78.1
NSE: Script scanning 192.168.78.1.
Initiating NSE at 14:44
Completed NSE at 14:45, 57.73s elapsed
Initiating NSE at 14:45
Completed NSE at 14:45, 1.01s elapsed
Initiating NSE at 14:45
Completed NSE at 14:45, 0.00s elapsed
Nmap scan report for 192.168.78.1
Host is up (0.024s latency).
Not shown: 999 closed tcp ports (reset), 982 closed udp ports (port-unreach)
PORT      STATE         SERVICE         VERSION
53/tcp    open          domain          dnsmasq 2.78
53/udp    open          domain          dnsmasq 2.78
| dns-nsid: 
|_  bind.version: dnsmasq-2.78
67/udp    open          dhcps?
68/udp    open|filtered dhcpc
123/udp   open          ntp             NTP v4 (unsynchronized)
| ntp-info: 
|_  receive time stamp: 2024-05-16T06:44:27
1000/udp  open|filtered ock
1051/udp  open|filtered optima-vnet
10080/udp open|filtered amanda
20424/udp open|filtered unknown
20465/udp open|filtered unknown
21948/udp open|filtered unknown
22914/udp open|filtered unknown
32776/udp open|filtered sometimes-rpc16
40622/udp open|filtered unknown
42627/udp open|filtered unknown
49170/udp open|filtered unknown
49210/udp open|filtered unknown
62677/udp open|filtered unknown
64080/udp open|filtered unknown
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port67-UDP:V=7.95%I=7%D=5/16%Time=6645AAE1%P=x86_64-pc-linux-gnu%r(DHCP
SF:_INFORM,12C,"\x02\x01\x06\0\x01#Eg\0\0\0\0\xff\xff\xff\xff\0\0\0\0\0\0\
SF:0\0\0\0\0\0\0\x0e5\xd4\xd8Q\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0
SF:\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\
SF:0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0
SF:\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\
SF:0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0
SF:\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\
SF:0\0\0c\x82Sc5\x01\x056\x04\xc0\xa8N\x01\xff\0\0\0\0\0\0\0\0\0\0\0\0\0\0
SF:\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\
SF:0");
MAC Address: 32:49:58:83:25:CD (Unknown)
Device type: general purpose
Running: Linux 3.X|4.X
OS CPE: cpe:/o:linux:linux_kernel:3 cpe:/o:linux:linux_kernel:4
OS details: Linux 3.2 - 4.14
Uptime guess: 0.020 days (since Thu May 16 14:15:48 2024)
Network Distance: 1 hop
TCP Sequence Prediction: Difficulty=262 (Good luck!)
IP ID Sequence Generation: All zeros

Host script results:
|_clock-skew: 6s

TRACEROUTE
HOP RTT      ADDRESS
1   23.91 ms 192.168.78.1

NSE: Script Post-scanning.
Initiating NSE at 14:45
Completed NSE at 14:45, 0.00s elapsed
Initiating NSE at 14:45
Completed NSE at 14:45, 0.00s elapsed
Initiating NSE at 14:45
Completed NSE at 14:45, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 1199.87 seconds
           Raw packets sent: 2591 (120.823KB) | Rcvd: 2184 (123.830KB)
```
## Synced and Added to eufy App
### Nmap TCP Intense Scan Result
```
Starting Nmap 7.94 ( https://nmap.org ) at 2024-05-05 17:54 AWST
NSE: Loaded 156 scripts for scanning.
NSE: Script Pre-scanning.
Initiating NSE at 17:54
Completed NSE at 17:54, 0.00s elapsed
Initiating NSE at 17:54
Completed NSE at 17:54, 0.00s elapsed
Initiating NSE at 17:54
Completed NSE at 17:54, 0.00s elapsed
Initiating ARP Ping Scan at 17:54
Scanning 203.13.69.113 [1 port]
Completed ARP Ping Scan at 17:54, 0.54s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 17:54
Completed Parallel DNS resolution of 1 host. at 17:54, 0.16s elapsed
Initiating SYN Stealth Scan at 17:54
Scanning CPE-69-113.dsl.OntheNet.net (203.13.69.113) [65535 ports]
Discovered open port 6668/tcp on 203.13.69.113
Completed SYN Stealth Scan at 17:54, 14.79s elapsed (65535 total ports)
Initiating Service scan at 17:54
Scanning 1 service on CPE-69-113.dsl.OntheNet.net (203.13.69.113)
Completed Service scan at 17:57, 179.19s elapsed (1 service on 1 host)
Initiating OS detection (try #1) against CPE-69-113.dsl.OntheNet.net (203.13.69.113)
NSE: Script scanning 203.13.69.113.
Initiating NSE at 17:57
Completed NSE at 17:57, 14.48s elapsed
Initiating NSE at 17:57
Completed NSE at 17:57, 1.37s elapsed
Initiating NSE at 17:57
Completed NSE at 17:57, 0.00s elapsed
Nmap scan report for CPE-69-113.dsl.OntheNet.net (203.13.69.113)
Host is up (0.0070s latency).
Not shown: 65534 closed tcp ports (reset)
PORT     STATE SERVICE VERSION
6668/tcp open  irc?
|_irc-info: Unable to open connection
MAC Address: 30:49:58:83:25:CD (Unknown)
Device type: general purpose
Running: Linux 3.X|4.X
OS CPE: cpe:/o:linux:linux_kernel:3 cpe:/o:linux:linux_kernel:4
OS details: Linux 3.2 - 4.9
Uptime guess: 0.004 days (since Sun May  5 17:52:46 2024)
Network Distance: 1 hop
TCP Sequence Prediction: Difficulty=263 (Good luck!)
IP ID Sequence Generation: All zeros

TRACEROUTE
HOP RTT     ADDRESS
1   7.01 ms CPE-69-113.dsl.OntheNet.net (203.13.69.113)

NSE: Script Post-scanning.
Initiating NSE at 17:57
Completed NSE at 17:57, 0.00s elapsed
Initiating NSE at 17:57
Completed NSE at 17:57, 0.00s elapsed
Initiating NSE at 17:57
Completed NSE at 17:57, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 212.06 seconds
           Raw packets sent: 65605 (2.887MB) | Rcvd: 65569 (2.624MB)
```
### Nmap UDP Intense Scan Results
```
Starting Nmap 7.94 ( https://nmap.org ) at 2024-05-05 18:00 AWST
NSE: Loaded 156 scripts for scanning.
NSE: Script Pre-scanning.
Initiating NSE at 18:00
Completed NSE at 18:00, 0.00s elapsed
Initiating NSE at 18:00
Completed NSE at 18:00, 0.00s elapsed
Initiating NSE at 18:00
Completed NSE at 18:00, 0.00s elapsed
Initiating ARP Ping Scan at 18:00
Scanning 203.13.69.113 [1 port]
Completed ARP Ping Scan at 18:00, 0.41s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 18:00
Completed Parallel DNS resolution of 1 host. at 18:00, 0.00s elapsed
Initiating SYN Stealth Scan at 18:00
Scanning CPE-69-113.dsl.OntheNet.net (203.13.69.113) [1000 ports]
Discovered open port 6668/tcp on 203.13.69.113
Completed SYN Stealth Scan at 18:00, 0.61s elapsed (1000 total ports)
Initiating UDP Scan at 18:00
Scanning CPE-69-113.dsl.OntheNet.net (203.13.69.113) [1000 ports]
Increasing send delay for 203.13.69.113 from 0 to 50 due to max_successful_tryno increase to 5
Increasing send delay for 203.13.69.113 from 50 to 100 due to max_successful_tryno increase to 6
Warning: 203.13.69.113 giving up on port because retransmission cap hit (6).
Increasing send delay for 203.13.69.113 from 100 to 200 due to 11 out of 11 dropped probes since last increase.
UDP Scan Timing: About 7.51% done; ETC: 18:07 (0:06:22 remaining)
Increasing send delay for 203.13.69.113 from 200 to 400 due to 11 out of 12 dropped probes since last increase.
Increasing send delay for 203.13.69.113 from 400 to 800 due to 11 out of 11 dropped probes since last increase.
UDP Scan Timing: About 10.94% done; ETC: 18:09 (0:08:16 remaining)
UDP Scan Timing: About 13.86% done; ETC: 18:11 (0:09:26 remaining)
UDP Scan Timing: About 17.07% done; ETC: 18:12 (0:10:02 remaining)
UDP Scan Timing: About 36.40% done; ETC: 18:14 (0:09:23 remaining)
UDP Scan Timing: About 42.46% done; ETC: 18:15 (0:08:38 remaining)
UDP Scan Timing: About 48.14% done; ETC: 18:15 (0:07:53 remaining)
UDP Scan Timing: About 53.60% done; ETC: 18:15 (0:07:07 remaining)
UDP Scan Timing: About 58.81% done; ETC: 18:15 (0:06:21 remaining)
UDP Scan Timing: About 64.04% done; ETC: 18:15 (0:05:34 remaining)
Discovered open port 123/udp on 203.13.69.113
UDP Scan Timing: About 69.50% done; ETC: 18:15 (0:04:45 remaining)
UDP Scan Timing: About 74.73% done; ETC: 18:15 (0:03:57 remaining)
UDP Scan Timing: About 80.00% done; ETC: 18:15 (0:03:09 remaining)
UDP Scan Timing: About 85.21% done; ETC: 18:15 (0:02:20 remaining)
UDP Scan Timing: About 90.37% done; ETC: 18:15 (0:01:31 remaining)
UDP Scan Timing: About 95.41% done; ETC: 18:16 (0:00:44 remaining)
Completed UDP Scan at 18:16, 998.15s elapsed (1000 total ports)
Initiating Service scan at 18:16
Scanning 25 services on CPE-69-113.dsl.OntheNet.net (203.13.69.113)
Service scan Timing: About 7.69% done; ETC: 18:30 (0:12:12 remaining)
Completed Service scan at 18:19, 173.13s elapsed (26 services on 1 host)
Initiating OS detection (try #1) against CPE-69-113.dsl.OntheNet.net (203.13.69.113)
NSE: Script scanning 203.13.69.113.
Initiating NSE at 18:19
Completed NSE at 18:21, 76.13s elapsed
Initiating NSE at 18:21
Completed NSE at 18:21, 1.44s elapsed
Initiating NSE at 18:21
Completed NSE at 18:21, 0.00s elapsed
Nmap scan report for CPE-69-113.dsl.OntheNet.net (203.13.69.113)
Host is up (0.074s latency).
Not shown: 999 closed tcp ports (reset), 975 closed udp ports (port-unreach)
PORT      STATE         SERVICE        VERSION
6668/tcp  open          irc?
|_irc-info: Unable to open connection
68/udp    open|filtered dhcpc
123/udp   open          ntp            NTP v4 (unsynchronized)
| ntp-info: 
|_  receive time stamp: 2024-05-05T10:19:55
434/udp   open|filtered mobileip-agent
1024/udp  open|filtered unknown
1031/udp  open|filtered iad2
1035/udp  open|filtered mxxrlogin
1064/udp  open|filtered jstel
1080/udp  open|filtered socks
9103/udp  open|filtered bacula-sd
17585/udp open|filtered unknown
17762/udp open|filtered unknown
18869/udp open|filtered unknown
19154/udp open|filtered unknown
19728/udp open|filtered unknown
19792/udp open|filtered unknown
20120/udp open|filtered unknown
20126/udp open|filtered unknown
20411/udp open|filtered unknown
20791/udp open|filtered unknown
31365/udp open|filtered unknown
41058/udp open|filtered unknown
41446/udp open|filtered unknown
44101/udp open|filtered unknown
49198/udp open|filtered unknown
61319/udp open|filtered unknown
MAC Address: 30:49:58:83:25:CD (Unknown)
Device type: general purpose
Running: Linux 3.X|4.X
OS CPE: cpe:/o:linux:linux_kernel:3 cpe:/o:linux:linux_kernel:4
OS details: Linux 3.2 - 4.9
Uptime guess: 0.020 days (since Sun May  5 17:52:47 2024)
Network Distance: 1 hop
TCP Sequence Prediction: Difficulty=263 (Good luck!)
IP ID Sequence Generation: All zeros

Host script results:
|_clock-skew: 8s

TRACEROUTE
HOP RTT      ADDRESS
1   74.27 ms CPE-69-113.dsl.OntheNet.net (203.13.69.113)

NSE: Script Post-scanning.
Initiating NSE at 18:21
Completed NSE at 18:21, 0.00s elapsed
Initiating NSE at 18:21
Completed NSE at 18:21, 0.00s elapsed
Initiating NSE at 18:21
Completed NSE at 18:21, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 1253.05 seconds
           Raw packets sent: 2630 (122.034KB) | Rcvd: 2014 (115.420KB)
```

