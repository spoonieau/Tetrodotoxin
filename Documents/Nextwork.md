 
#Network
##Factory Reset Mode

- Unit will create a AP With the SSID of ```eufy RoboVac L70 Hybrid-abcd``` and no password.
- When device is in AP mode it has a DHCP Server.
- Device AP mode IP Address ```192.168.78.1```
### Nmap TCPIP Intense Scan Results
> nmap -p 1-65535 -T4 -A -v 192.168.78.1
> Starting Nmap 7.95 ( https://nmap.org ) at 2024-05-16 15:11 AWST
> NSE: Loaded 157 scripts for scanning.
> NSE: Script Pre-scanning.
> Initiating NSE at 15:11
> Completed NSE at 15:11, 0.00s elapsed
> Initiating NSE at 15:11
> Completed NSE at 15:11, 0.00s elapsed
> Initiating NSE at 15:11
> Completed NSE at 15:11, 0.00s elapsed
> Initiating ARP Ping Scan at 15:11
> Scanning 192.168.78.1 [1 port]
> Completed ARP Ping Scan at 15:11, 0.11s elapsed (1 total hosts)
> Initiating Parallel DNS resolution of 1 host. at 15:11
> Completed Parallel DNS resolution of 1 host. at 15:11, 13.00s elapsed
> Initiating SYN Stealth Scan at 15:11
> Scanning 192.168.78.1 [65535 ports]
> Discovered open port 53/tcp on 192.168.78.1
> Completed SYN Stealth Scan at 15:12, 12.08s elapsed (65535 total ports)
> Initiating Service scan at 15:12
> Scanning 1 service on 192.168.78.1
> Completed Service scan at 15:12, 6.07s elapsed (1 service on 1 host)
> Initiating OS detection (try #1) against 192.168.78.1
> NSE: Script scanning 192.168.78.1.
> Initiating NSE at 15:12
> Completed NSE at 15:12, 8.24s elapsed
> Initiating NSE at 15:12
> Completed NSE at 15:12, 0.00s elapsed
> Initiating NSE at 15:12
> Completed NSE at 15:12, 0.00s elapsed
> Nmap scan report for 192.168.78.1
> Host is up (0.0092s latency).
> Not shown: 65534 closed tcp ports (reset)
> PORT   STATE SERVICE VERSION
> 53/tcp open  domain  dnsmasq 2.78
> | dns-nsid:
> |_  bind.version: dnsmasq-2.78
> MAC Address: 32:49:58:83:25:CD (Unknown)
> Device type: general purpose
> Running: Linux 3.X|4.X
> OS CPE: cpe:/o:linux:linux_kernel:3 cpe:/o:linux:linux_kernel:4
> OS details: Linux 3.2 - 4.14
> Uptime guess: 0.039 days (since Thu May 16 14:15:48 2024)
> Network Distance: 1 hop
> TCP Sequence Prediction: Difficulty=257 (Good luck!)
> IP ID Sequence Generation: All zeros

> TRACEROUTE
> HOP RTT     ADDRESS
> 1   9.17 ms 192.168.78.1

> NSE: Script Post-scanning.
> Initiating NSE at 15:12
> Completed NSE at 15:12, 0.00s elapsed
> Initiating NSE at 15:12
> Completed NSE at 15:12, 0.00s elapsed
> Initiating NSE at 15:12
> Completed NSE at 15:12, 0.00s elapsed
> Read data files from: /usr/bin/../share/nmap
> OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
> Nmap done: 1 IP address (1 host up) scanned in 40.89 seconds
>           Raw packets sent: 67181 (2.957MB) | Rcvd: 65655 (2.627MB)

