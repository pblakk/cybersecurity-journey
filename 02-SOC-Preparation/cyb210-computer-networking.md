# CYB 210 — Computer Networking

Completed: December 2025

## Topics covered
- Network architectures — examining different approaches
  to network design and their security implications
- IPv4 and IPv6 addressing — designing addressing schemes
  to meet specific architectural requirements
- Subnetting — calculating and implementing subnets using
  CIDR notation for network segmentation
- VLANs — configuring virtual LANs to segment traffic and
  isolate sensitive systems from general network traffic
- Routing — static routing configuration and how routers
  determine paths for network traffic
- NAT, DHCP, and DNS — core protocol configuration and
  administration on network devices
- Network security fundamentals — securing switches,
  implementing network segmentation, and access control
- Guest wireless network configuration — isolating guest
  traffic from internal business systems
- Network troubleshooting — diagnosing and resolving
  connectivity issues in complex multi-device environments
- Network administration — configuring and managing
  routers, switches, and other network devices

## Tools and resources used
- **Cisco Packet Tracer** — primary lab environment for
  all network configuration and simulation labs
- **uCertify** — interactive learning platform for
  concept reinforcement
- **All-in-One CompTIA Network+ Certification Exam Guide**
  by Mike Meyers — primary textbook

## Projects completed

### Network configuration labs
Built, troubleshot, and reconfigured networks in Cisco
Packet Tracer across multiple complex multi-hour labs.
Configured VLANs, DHCP, static routing, and verified
connectivity throughout.

### IP addressing and subnetting design
Designed IPv4 and IPv6 addressing schemes to meet
specific architectural requirements including network
segmentation and device capacity planning.

### Guest wireless network configuration
Configured a guest wireless network isolated from
internal business systems using VLANs and access
control — applying security principles to a real-world
common network scenario.

### Network modification and analysis projects
Completed major projects involving modifying existing
network configurations, analyzing network diagrams,
and troubleshooting router and switch setups.

## What I understand now that I didn't before
- IPv6 is not optional anymore. The exhaustion of IPv4
  addresses means real-world networks increasingly use
  IPv6, and malware increasingly targets IPv6 traffic
  because many security tools are still tuned primarily
  for IPv4.
- VLANs are a fundamental security control, not just
  an administrative convenience. Proper VLAN configuration
  is what prevents a compromised guest device from
  reaching internal systems — misconfiguration creates
  a direct path for lateral movement.
- Subnetting is a security architecture decision. How
  you divide a network determines what can communicate
  with what by default. Getting it wrong creates
  unintended trust relationships between systems.
- Network troubleshooting is systematic elimination.
  Working through a connectivity problem layer by layer
  and device by device is the same disciplined methodology
  used in malware analysis — eliminate what it isn't
  until you find what it is.
- NAT creates a false sense of security. Many organizations
  treat NAT as a security boundary when it is not — malware
  can and does communicate outbound through NAT without
  any special privileges.

## Connection to malware analysis
- **VLAN knowledge connects directly to lateral movement
  analysis.** When analyzing how malware spread through
  an environment, understanding VLAN boundaries tells
  you which systems the malware could and could not
  reach from its initial foothold.
- **Subnetting connects to C2 traffic analysis.** When
  a malware sample makes network connections, knowing
  whether the destination IP is in the same subnet,
  a different internal subnet, or an external address
  immediately tells you something about its behavior
  and intent.
- **DHCP and DNS knowledge connects to malware detection.**
  Malware frequently abuses DNS for C2 communication —
  DNS tunneling, domain generation algorithms, and fast
  flux hosting all exploit how DNS works. Understanding
  legitimate DNS behavior makes malicious DNS traffic
  recognizable.
- **NAT understanding connects to C2 evasion techniques.**
  Malware uses outbound connections through NAT because
  most organizations allow outbound traffic freely.
  Understanding why NAT does not provide security explains
  why so much malware C2 uses outbound HTTP and HTTPS.
- **Packet Tracer experience connects to network forensics.**
  Configuring how traffic flows through a network makes
  reconstructing that traffic from packet captures and
  logs significantly more intuitive.

## What I want to go deeper on
- DNS abuse by malware — tunneling, DGA, and fast flux
  techniques and how to detect them in packet captures
  and DNS logs
- IPv6 security implications — how malware uses IPv6
  to evade IPv4-focused security controls
- Network forensics — reconstructing malware activity
  from NetFlow data, DHCP logs, and DNS query logs
- Advanced VLAN security — VLAN hopping attacks and
  how malware attempts to cross VLAN boundaries
- CompTIA Network+ certification — the Mike Meyers
  textbook from this course is the standard Network+
  prep resource and the certification validates this
  knowledge formally
