# CYB 310 Project Three — Network Reconfiguration & Firewall Policy

**Course:** CYB 310 Network Defense
**Tool:** GNS3 + OPNsense

## Scenario

Reconfigured a network to reflect organizational restructuring 
(departments merged into Customer Experience + HR, servers 
isolated into dedicated VLAN) and implemented firewall traffic 
flow policy.

## Network Reconfiguration

- CustExpSwitch — 6 PCs on VLAN 2 (192.168.2.0/24)
- HRSwitch — 3 PCs on VLAN 3 (192.168.3.0/24)
- ServerSwitch — WebServer + AuthServer on VLAN 4 (192.168.4.0/24)
- Dedicated CoreRouter and ServerRouter, separate from 
  department traffic

## Firewall Rules Configured (OPNsense)

1. NAT port forward — WAN port 80 → WebServer (192.168.4.2)
2. NAT port forward — WAN port 443 → WebServer (192.168.4.2)
3. Manual block rule — WAN port 80 → all other destinations
4. Manual block rule — WAN port 443 → all other destinations

**Critical detail:** Allow rules must sit above block rules — 
firewalls process top-down and stop at first match.

## Key Lesson

VLANs alone provide only logical separation; actual security 
enforcement comes from router ACLs and firewall rules. 
Segmentation without enforcement provides no real protection — 
this was direct instructor feedback on the Module 5 milestone 
that shaped this implementation.

## CIA Triad Impact

- **Confidentiality** — only WebServer reachable from WAN, 
  AuthServer isolated
- **Integrity** — controlled routing paths make unauthorized 
  modification harder
- **Availability** — segmentation prevents one department's 
  traffic issues from affecting servers
