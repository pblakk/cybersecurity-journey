# CYB 220 — Network Security

Completed: C-1 JAN-MAR 2026

## Topics covered
- Intrusion detection and prevention systems (IDS/IPS) —
  network-based and host-based variants (NIPS, NIDS, HIPS, HIDS)
- Technology evaluation — balancing effectiveness, cost, and
  organizational constraints to recommend security solutions
- Network segmentation strategy — isolating network zones
  using host-based and network-based firewall policies
- Access control lists (ACLs) — configuring extended ACLs
  on Cisco IOS routers in Packet Tracer
- FTP server access control — applying least privilege principles
- Windows Group Policy hardening — configuring GPO settings
  to reduce attack surface on Windows endpoints
- Virtualization and sandboxing — using GNS3 to safely test
  configurations before production deployment
- Fundamental security design principles — applying concepts
  such as least privilege and defense in depth to real scenarios
- Network traffic flow policy and enforcement — firewall rules,
  segmentation, and isolation strategies
- Splunk — log ingestion, SPL queries, and basic incident analysis
- Secure vs. insecure protocols — SSH vs Telnet, FTPS vs FTP,
  HTTPS vs HTTP

## Tools used

### Virtualization & simulation
- **GNS3** — network emulation for sandboxing lab environments
- **Cisco Packet Tracer** — network simulation, firewall and ACL configuration
- **CompTIA CertMaster Labs** — browser-based virtual lab environment

### Security & analysis
- **Wireshark** — packet capture and protocol analysis
- **Nmap** — network discovery and vulnerability scanning
- **PuTTY** — SSH client for secure remote access
- **WinSCP** — secure file transfer via SCP/SFTP
- **SET (Social Engineering Toolkit)** — penetration testing framework
- **SQL injection tools** — vulnerability exploitation and detection

### Operating systems & configuration
- **Windows Group Policy Editor** — system hardening and policy enforcement
- **Windows Firewall** — host-based access control configuration
- **Cisco IOS** — extended ACL configuration on routers

### Protocols & services
- FTP/FTPS — file transfer with access control
- SMTP/POP3 — email traffic simulation
- HTTP/HTTPS — web traffic and encrypted flows
- SSH/Telnet — secure vs. insecure remote access comparison

### SIEM & logging
- **Splunk** — log ingestion, SPL queries, and basic incident analysis

## Projects completed

### Project 1 — Virtual systems and networking concept brief
Configured group policy settings and network resources in a
GNS3 sandboxed environment. Hardened a Windows endpoint by
applying specific GPO settings including hiding Control Panel
items, removing Task Manager, and disabling insecure protocols.
Wrote a conceptual justification of virtualization benefits and
drawbacks for a system administrator audience.

### Project 2 — Network segmentation strategy
Configured host-based and network-based firewall policies in
Cisco Packet Tracer. Set up FTP server access control applying
least privilege. Configured extended ACLs on Cisco IOS routers.
Wrote a rationale explaining how the configuration achieved
network segmentation, least privilege, and isolation.

### Project 3 — Network protection technology evaluation
Evaluated NIPS, NIDS, HIPS, and HIDS against effectiveness
and cost criteria. Applied a fundamental security design
principle to justify a recommended network protection approach
for a fictional organization. Balanced technical capability
against business constraints including budget, staffing, and
implementation time.

## What I understand now that I didn't before
- IDS vs IPS is not just a technical distinction — it is a
  business decision. An IPS can block threats automatically
  but can also cause network outages if misconfigured. An IDS
  only detects and alerts, which is safer but requires human
  response. Choosing between them depends on the organization's
  risk tolerance and operational constraints, not just which
  one is more effective technically.
- Least privilege is not just a concept — it is something you
  physically configure. Setting FTP server permissions and
  firewall ACLs forces you to think about exactly who needs
  access to what and nothing more.
- Network segmentation is how you contain damage. If every
  system is on the same flat network, malware that reaches
  one machine can reach all of them. Segmentation with firewall
  policies limits lateral movement.
- Sandboxing with GNS3 showed me why malware analysts use
  isolated virtual environments. You can test dangerous or
  unknown configurations without risking production systems.
- Group Policy is a real attack surface. The settings I
  hardened are exactly the kinds of configurations attackers
  look for when they land on a Windows machine.

## Connection to malware analysis
- **IDS/IPS evaluation connects directly to C2 detection.**
  Understanding how NIDS monitors network traffic for suspicious
  patterns is the same skill used to detect malware beaconing
  behavior.
- **Network segmentation limits malware lateral movement.**
  Firewall ACLs isolating network zones are the defensive
  countermeasure to lateral movement — a technique malware
  analysts study constantly.
- **Group Policy hardening removes malware footholds.**
  The settings I configured are settings malware actively
  manipulates after gaining access to a Windows host.
- **GNS3 sandboxing is the same principle as malware analysis
  lab environments.** Executing unknown configurations in an
  isolated VM before touching production is identical in concept
  to executing malware samples safely for dynamic analysis.
- **Splunk SPL queries connect to threat hunting.**
  Malware generates logs — process creation, network connections,
  registry changes. Knowing how to query those logs in Splunk
  is how a defensive analyst finds evidence of compromise.
- **Insecure vs secure protocols matter for malware analysis.**
  Malware frequently exploits unencrypted protocols because
  traffic is visible and injectable.

## What I want to go deeper on
- Network traffic analysis at the packet level — reading
  captures fluently to identify C2 traffic and beaconing.
  Covered by Practical Packet Analysis in Phase 2.
- Splunk at a deeper level — correlation searches, dashboards,
  and threat hunting against malware-generated logs.
- IDS tuning and alert management — reducing false positives
  without missing real threats. Connects to writing effective
  YARA rules in Phase 2.
- How malware specifically evades network detection — C2
  communication designed to blend with legitimate traffic.
  Covered by Evasive Malware in Phase 3.
- Firewall ACL logic at enterprise scale — managing hundreds
  of rules without creating exploitable gaps.
