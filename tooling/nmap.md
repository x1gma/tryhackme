# NMap

Recon on reachable ports and services

### Scans

#### Network
nmap -sn 192.168.0.0/24 - Ping sweep on network using ICMP/ARP

#### Standard 
-sT TCP scan (performs tcp handshake)
-sU UDP scan (fire&forget UDP packets)

-sV Version scan

-p X-Y port scan range 
-p- all ports

#### FW evasion
-sS SYN scan (stealth scan, sends RST)

#### FW evasion^2 - may be unreliable for windows/cisco NICs
-sN NULL scan (no flags, expects RST as per RFC)
-sF FIN scan (FIN flag, expects RST as per RFC)
-sX XMAS scan (malformed flags, expects RST as per RFC)

### Other 

-A  aggressive mode (service&os detection, traceroute, script scan)
-oA all normal format outputs
-O  OS detection
-vv verbose
-TX timing speed X=1..5

### Scripts

Scipt docs and categories: https://nmap.org/book/nse-usage.html
Local list in /usr/share/nmap/scripts

-sC - activate default scripts
--script=xyz activate scripts
--script-args xyz.arg1=123 - set argument for script xyz
