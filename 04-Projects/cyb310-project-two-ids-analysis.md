# CYB 310 Project Two — IDS Analysis Paper

**Course:** CYB 310 Network Defense
**Format:** 2-4 page analysis paper

## Critical Thinking Questions

**Confidentiality** — Best addressed by NIDS sensors with 
deep packet inspection, which monitor traffic for 
unauthorized data leaving the network (exfiltration, C2 
beaconing).

**Integrity** — Indicators include unusual file system 
activity (ransomware encryption), unauthorized registry 
modifications (persistence mechanisms), and C2 beaconing 
patterns.

**Availability** — Detected through traffic volume anomalies 
(DoS/DDoS signatures — SYN floods, ICMP floods) and 
protocol anomaly detection for malformed packets.

## Scenario — Meridian Financial Services

Fictitious mid-sized financial firm, two buildings, 280 
employees, handling client PII and trading algorithms under 
GLBA/SOX regulation.

## IDS Components Selected

1. **NIDS sensors at both building perimeters** — signature 
   tuned for financial malware (Dridex, TrickBot) and 
   phishing callback detection.
2. **HIDS on servers storing client financial data** — 
   monitors unauthorized file access, privilege escalation, 
   and insider threat indicators.

## Key Lesson

Layered IDS coverage (network + host) catches what a 
single detection layer misses — NIDS for perimeter threats, 
HIDS for insider threats and post-breach activity.
