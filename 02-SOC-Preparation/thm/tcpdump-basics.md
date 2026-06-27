# TCPdump Basics — TryHackMe

Completed: June 2026
Path: Cyber Security 101

## Key Commands Learned

# Read from file
tcpdump -r traffic.pcap -n

# Filter by protocol
tcpdump -r traffic.pcap -n icmp
tcpdump -r traffic.pcap -n arp
tcpdump -r traffic.pcap port 53

# Count packets
tcpdump -r traffic.pcap -n icmp | wc -l

# Filter by TCP flags — RST only
tcpdump -r traffic.pcap -n 'tcp[tcpflags] == tcp-rst'

# Filter by packet size
tcpdump -r traffic.pcap -n greater 15000

# Show MAC addresses
tcpdump -r traffic.pcap -e arp

## Key Concepts

- -r reads from a pcap file instead of live capture
- -n prevents DNS resolution showing raw IPs
- -e shows MAC addresses in output
- port 53 filters DNS traffic
- Pipe to wc -l to count packets automatically
- tcp[tcpflags] == tcp-rst filters for RST-only packets
- greater [bytes] filters by packet size

## Observations

ARP requests reveal which host is asking for a MAC address —
useful for detecting ARP spoofing attacks where a malicious
host sends fake ARP replies to redirect traffic.

DNS queries on port 53 reveal what hostnames a host is
resolving — useful for detecting C2 beaconing where malware
regularly queries attacker-controlled domains.

RST flag packets indicate abrupt connection terminations —
useful for detecting port scanning where scanners send RST
to close connections quickly after probing.
