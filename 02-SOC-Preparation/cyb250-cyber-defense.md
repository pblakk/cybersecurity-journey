# CYB 250 — Cyber Defense

Completed: April 2026

## Topics covered
- System and network protection — securing Windows and
  Linux operating systems and applications against
  common attack vectors
- Threat modeling and analysis — using the STRIDE
  framework to model threats and analyzing real-world
  breaches including Sony and OPM to understand
  attack vectors and control failures
- Cybersecurity operations — implementing security
  policies, incident response plans, and password
  policies in organizational environments
- Cryptography principles — understanding the role
  of encryption in protecting information assets
  and securing communications
- Emerging trends — security implications of cloud
  computing, virtualization, and mobile technologies
- Human factors — social engineering defense,
  acceptable use policies, and security awareness
- Case study analysis — evaluating past data breaches
  to identify where security controls failed and
  recommending defensive improvements

## Tools used
- Virtual labs and simulations — testing security
  controls and analyzing malicious activity in
  controlled environments

## Projects completed

### Case study analyses
Evaluated real-world data breaches including Sony
and OPM to determine where security controls failed,
how attackers gained and maintained access, and what
defensive improvements would have prevented or
limited the damage.

### Final project — comprehensive defense strategy
Developed a defense strategy for a scenario-based
organization mitigating risks for a new headset
device. Applied threat modeling, security controls,
cryptography principles, and incident response
planning to produce a complete defensive posture
recommendation.

## What I understand now that I didn't before
- Threat modeling with STRIDE turns abstract risk
  into concrete, actionable categories. Every threat
  maps to Spoofing, Tampering, Repudiation, Information
  disclosure, Denial of service, or Elevation of
  privilege. Having that framework makes it possible
  to analyze any system or scenario systematically
  rather than trying to think of threats freeform.
- Cryptography is not optional in security — it is
  foundational. Every secure communication, every
  protected file, every authenticated session depends
  on cryptographic principles. Understanding how
  encryption works is what makes it possible to
  recognize when something is broken or being abused.
- Real breaches follow patterns. Studying Sony and
  OPM showed that most major incidents involve the
  same categories of failure — insufficient access
  controls, unpatched systems, inadequate monitoring,
  and slow detection. Recognizing those patterns
  makes them faster to identify in new scenarios.
- Emerging technologies introduce new attack surfaces
  faster than defenses mature. Cloud misconfiguration,
  mobile device management gaps, and virtualization
  escapes are growing categories of real-world attacks
  that defenders need to understand proactively.
- Human factors are not a soft topic — they are a
  hard security problem. Social engineering bypasses
  technical controls entirely. Acceptable use policies
  and security awareness training are technical
  controls expressed through behavior rather than code.

## Connection to malware analysis
- **STRIDE connects directly to malware classification.**
  Every malware family maps to STRIDE categories —
  ransomware is denial of service and tampering,
  spyware is information disclosure, rootkits involve
  elevation of privilege. Using STRIDE to frame malware
  analysis gives findings a structured, communicable
  format that defenders and incident responders
  immediately understand.
- **Cryptography is essential for malware analysis.**
  Malware uses encryption constantly — protecting C2
  communications, encrypting ransomware payloads,
  and obfuscating strings and configuration data.
  Understanding cryptographic principles is what
  allows analysts to recognize encryption in malware
  and sometimes reverse it.
- **Case study methodology connects to threat hunting.**
  Analyzing how past breaches unfolded — initial
  access, persistence, lateral movement, exfiltration
  — is the same analytical framework used in threat
  hunting and incident response when malware is
  detected in an environment.
- **Emerging technology security connects to evolving
  malware targeting.** Cloud-targeting malware, mobile
  malware, and virtualization-aware malware are growing
  rapidly. CYB 250 provided the context for why the
  malware landscape is evolving in those directions.
- **Incident response planning connects to malware
  triage workflows.** The structured IR process covered
  in CYB 250 — preparation, detection, containment,
  eradication, recovery — is the same workflow a
  malware analyst follows when a new sample is
  submitted for analysis in a real incident.

## What I want to go deeper on
- Cryptography as it applies specifically to malware —
  custom encryption implementations, XOR obfuscation,
  and how malware authors implement encryption poorly
  in ways analysts can exploit to decrypt C2 traffic
  or recover encrypted payloads
- STRIDE applied to specific malware families —
  mapping real malware behavior to the framework
  to build structured analysis reporting habits
- Cloud-targeting malware — how malware specifically
  abuses cloud infrastructure for C2, persistence,
  and data exfiltration
- Incident response for active malware infections —
  the specific triage, containment, and forensic
  workflow when the threat is confirmed malware
  rather than a generic security incident
