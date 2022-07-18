# Nmap

There are 1024 “well-known” ports and we can use nmap to quickly scan them and much more.

`nmap {flags} {IP}`

^by default nmap will run a 

Flags:

- `-vv` level 2 verbosity (use this for troubleshooting)
- `-p` specify port or port range (`-p-` scans all ports)
- `-oA` save nmap result in all 3 major formats
- `-sV` Service detection (important)
- `-A` Aggressive mode (not sneaky)

Scan types:

- `-sS` (Stealth but not actually, don’t use this) “Half-Open” [SYN, SYN/ACK, RST]
- `-sT` TCP scan
- `-sU` UDP scan
- `-sN` (NULL) empty TCP packet is sent [Stealthier]
- `-sF` (FIN) same as NULL but gracefully closes an active connection once done
- `-sX`  (XMAS) same as Null but with PSH, URG, and FIN flags

NOTE:

Due to their nature, -sU, -sN, -sF, and -sX will identify ports as open/filtered and not just “open”

Opened ports can also appear closed because Windows/Cisco respond to malformed packets with RST

## Make a network Map (Scanning Multiple Systems)

When we’re scanning multiple computers we first need to create a “network map” to determine which hosts are alive on the network

`nmap -sn {IP/24}` 

- Sends ICMP echo packets or ARP if on a local network
- Also sends TCP SYN packet to port 443 and TCP ACK (or TCP SYN if not run as root) to port 80

You can use a more manual approach approach via:

`nmap {flags} {IP/24}`

- `-sP` Ping network scan
- `-PR` ARP Discovery

## Scripts

For more info: [https://nmap.org/book/nse-usage.html](https://nmap.org/book/nse-usage.html)

Scripts are written in Lua and we use the `-sC` flag

- `--script = {script name}`
- `--script-args = {script arguments}`
- `grep “{script you want to look for}” /usr/share/nmap/scripts/script.db`

## Firewall Evasion

For more info: [https://nmap.org/book/man-bypass-firewalls-ids.html](https://nmap.org/book/man-bypass-firewalls-ids.html)

Problem:

Windows Firewall blocks ICMP packets (host with firewall will register as dead)

Solution:

- `-Pn` Nmap won’t ping hosts before scanning it, thus the target will always be treated as if it were alive [⭐]
    - If you’re already on the local network you can use ARP request instead of ping
- `-f` Fragments packets
- `--mtu {number}` same as “-f” but with more control over size of packets
    - Note that the number must be a multiple of 8
- `--scan-delay {time}ms` Adds a time delay between packets sent
- `--badsum`Used to determine if there is a firewall since firewalls respond automatically

## Things to keep in mind

There are 1024 “well-known” ports

<x.x.x.*> (*) means “all in range” 

TCP = Three way handshake (SYN [synchronize], SYN/ACK  [acknowledge], ACK)

- When a port is closed (SYN, RST [reset])

UDP = doesn't check if packet was received (SYN, ACK/RST)

ICMP = ping