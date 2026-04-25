# IT 212 — Introduction to Computer Networks

Completed: October 2025

## Topics covered
- OSI and TCP/IP models — understanding how data moves
  through network layers and the function of each layer
- Network topology design — planning and implementing
  network layouts including star topology for local and
  remote employees
- Network components — roles and functions of servers,
  clients, switches, routers, and firewalls in a network
- Hardware selection — choosing appropriate routers,
  switches, and other hardware to meet business requirements
- ISP research and selection — evaluating internet service
  providers based on organizational needs
- Basic network security — implementing firewalls and
  security measures to protect network infrastructure
- Network troubleshooting — identifying connectivity
  issues, conducting ping tests, and analyzing performance
- LAN design — designing local area networks for business
  environments

## Projects completed

### Milestone 1 — Network design
Planned a network infrastructure for a specific office
location. Selected topology, identified required components,
and designed the layout to support both local and remote
employees.

### Milestone 2 — ISP and hardware selection
Researched and recommended internet service providers and
networking hardware based on organizational requirements.
Balanced cost, performance, and security considerations.

### Final project — Secure network setup report
Submitted a comprehensive report on a secure network
design for a business expansion scenario based in
Fayetteville, NC. Covered infrastructure design, hardware
selection, ISP recommendation, security measures, and
troubleshooting approach.

## What I understand now that I didn't before
- Network design is a security decision from the start.
  Choosing a topology, placing firewalls, and selecting
  hardware all have security implications that cannot be
  bolted on after the fact — they have to be built in.
- The OSI model is not just academic. It is a practical
  framework for troubleshooting. When something breaks
  you work through the layers systematically — physical,
  data link, network, transport — until you find where
  the problem lives. That same systematic approach applies
  to analyzing malware behavior layer by layer.
- Firewalls are not a complete security solution. They
  control traffic at the network boundary but do nothing
  about threats already inside the network or threats
  delivered through permitted traffic like email
  attachments and web downloads.
- Hardware selection affects security posture. Cheap or
  end-of-life hardware often lacks security updates and
  modern protocol support — understanding this connection
  between infrastructure decisions and security outcomes
  started here.

## Connection to malware analysis
- **Network topology knowledge helps analysts understand
  malware spread.** Knowing how a network is laid out —
  where the segments are, where the firewalls sit, what
  can reach what — is essential context when tracing how
  malware moved through an environment after initial
  compromise.
- **OSI model connects to protocol-level malware analysis.**
  Malware operates at specific OSI layers. Network layer
  for C2 IP traffic, transport layer for port selection,
  application layer for protocol mimicry. Knowing the
  model tells you where to look for malicious activity.
- **Firewall knowledge connects to C2 evasion analysis.**
  Malware is specifically designed to bypass firewalls —
  using common ports like 80 and 443, encrypting traffic,
  and mimicking legitimate protocols. Understanding how
  firewalls work makes evasion techniques immediately
  recognizable.
- **Troubleshooting methodology connects to malware
  triage.** Ping tests, connectivity analysis, and
  systematic elimination of possibilities in IT 212
  is the same disciplined methodology used when working
  through an unknown malware sample.

## What I want to go deeper on
- Reading real packet captures in Wireshark against
  actual network traffic — Practical Packet Analysis
  in Phase 2 builds directly on this foundation
- How malware specifically bypasses firewalls and
  network controls — covered in Evasive Malware
  in Phase 3
- Network forensics — reconstructing attacker and
  malware activity from network logs and packet captures
- Advanced network design for malware analysis lab
  environments — isolating infected VMs from the host
  network safely
