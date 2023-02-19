# dos ddos distributed denial of service, botnets

DDOS involves botnet : robot network controled through a command & control center

## finding vuln machines : 
random scanning
hit-list scanning : delegate scanning to infected machine
topological : infected machines gives new machines to infect
local subnet scan : infected machines searches in her subnet
permutation : avoids reinfection, random high speed scan

## Malicious code propagation
central source, back-chaining, autonomous

## dos/ddos techniques
###volumetric attack : 
bandwidth bps; targets NTP, DNS, SSDP => flood attack, amplification attack througr broadcast
udp flood attack, icmp flood attack, ping of death (oversized ping) , smurf (icmp with spoofed ip so spoofed ip gets lots of icmp echo), pulse wave (repetitive ddos 10min each hour), 0-day, malformed IP, spoofed IP
TCP Selective Acknowledgment (SACK) panic attack = malformed maximum segment size (MSS) = integer overflow vulnerability in Linux Socket Buffer (SKB) 
D reflection DOS drdos

### protocol attacks
consuming resources other than bandwith : packet per second pps connection per second cps
connection state tables, firewall, ...
partial tcp 3way handshake / flood : syn flood, syn-ack, ack push ack, 
fragmentation (resources consumption), spoofed session, ack flood, tcp state, rst, tcp sack panic
spoofed session : syn-ack (create many sessions), spoofed ack, tcp

### app layer attacks
application vulns, connection openings, difficult to detect, buffer overflow, request per seconds rps, disabling access through missed password
http flood, slowloris (multiple opened connection), udp app layer, ddos extortion
http get (open connection), post (incomplete post)

### hardware
permanent dos pdos / phlashing = hardware dos / bricking

## Defenses / Detection techniques / countermeasures
packet filtering, 
Turn off the Character Generator Protocol (CHARGEN) 
traffic analysis : sequential change-point, statistic, activity profiling, wavelet-based signal analysis (spectrum)
absorbing, degrading, shutting down
egress filtering, applied by Network service providers (packet analysis, detects spoofed ip)
ingress (ISP techniques)
tcp syn cookie protection

## Tools
attack : High Orbit Ion Cannon (HOIC), LOIC, XOIC, HULK, Metasploit, tor’s hammer, pyloris, andosid
countermeasures/honeypots : sshhipot, artillery, cowrie, kfsensor
against botnets : rfc3704 filtering : acl filter, cisco source ip reputation, black-hole (unnotified dropped packets)
anti ddos guardian, Akamai DDoS, Kaspersky DDoS, Corero DDoS, BlockDoS 
hardware : TCP Intercept on Cisco IOS Software : specify the networks, FortiDDoS (machine learning), ddos protector (multi layer), terabit, a10 thunder,
 
## History
azure 2021 : 2.4 Tbps, 10mins dos
