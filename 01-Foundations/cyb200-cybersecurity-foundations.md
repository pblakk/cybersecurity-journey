# CYB 200 — Cybersecurity Foundations

Completed: August 2025

## Topics covered
- CIA Triad — confidentiality, integrity, and availability
  as the framework for evaluating all security decisions
- Principle of Least Privilege (PoLP) — limiting access
  rights to only what is necessary for a given role
- Zero Trust architecture — never trust, always verify,
  regardless of network location
- Adversarial vs environmental threats — distinguishing
  between intentional attacks and accidental or natural
  disruptions and how response strategies differ
- Threat and risk management — identifying, categorizing,
  and prioritizing security risks
- Security policies and governance — developing
  organizational security policies and understanding
  the legal and ethical factors that shape them
- Incident Response Planning (IRP) — creating structured
  plans for detecting, containing, and recovering from
  security breaches
- Role-Based Access Control (RBAC) — configuring access
  matrices that assign permissions based on job function
- Security awareness and culture — training employees to
  recognize threats and adopt security-conscious behaviors
- Proactive security mindset — anticipating threats before
  they materialize rather than reacting after the fact

## Projects completed

### Project 1 — Security awareness training case study
Created training materials to help employees identify
adversarial and environmental threats. Focused on building
security culture through practical, accessible guidance.

### Project 2 — Incident analysis brief
Analyzed a security incident to identify what happened,
how it happened, and what response strategies should be
applied. Developed structured thinking around incident
response workflows.

### Project 3 — Technical brief: proactive security mindset
Developed a brief advocating for proactive security
practices — identifying vulnerabilities and closing gaps
before adversaries can exploit them.

## What I understand now that I didn't before
- The CIA Triad is not just a concept to memorize — it is
  a decision-making tool. Every security control can be
  evaluated against it. Does this protect confidentiality?
  Does it preserve integrity? Does it ensure availability?
  Those three questions cut through a lot of complexity.
- Adversarial and environmental threats require fundamentally
  different responses. An attacker adapts to your defenses.
  A flood does not. Treating them the same leads to
  security strategies that fail against one or the other.
- Zero Trust reframes how you think about network security.
  The assumption that internal traffic is safe is exactly
  what malware exploits after it gains an initial foothold.
  Zero Trust eliminates that assumption entirely.
- Incident response is a structured process, not a panic
  response. Having a plan before an incident happens is
  what separates organizations that recover quickly from
  ones that don't.
- Security culture matters as much as technical controls.
  The most hardened network can be compromised by one
  employee clicking a phishing link. Human factors are
  not separate from security — they are central to it.

## Connection to malware analysis
- **CIA Triad connects to malware impact assessment.**
  When analyzing malware, one of the first questions is
  what it targets — does it steal data (confidentiality),
  modify files (integrity), or lock systems (availability)?
  Ransomware attacks availability. Spyware attacks
  confidentiality. The triad frames the impact immediately.
- **Adversarial threat mindset is the malware analyst's
  default mode.** Malware is written by adversaries who
  adapt, evade, and evolve. CYB 200 built the mental model
  of thinking like an attacker — which is exactly what
  reverse engineering requires.
- **Incident response connects to malware triage.**
  The structured incident response process — detect,
  contain, analyze, recover — is the same workflow a
  malware analyst follows when a new sample is submitted
  for analysis. CYB 200 built the procedural foundation.
- **Least privilege connects to malware privilege
  escalation.** Malware frequently attempts to escalate
  privileges beyond what the compromised account should
  have. Understanding least privilege makes privilege
  escalation techniques immediately recognizable as
  violations of a fundamental security principle.
- **Proactive mindset connects to threat hunting.**
  Threat hunting is proactive malware detection —
  looking for evidence of compromise before an alert
  fires. CYB 200 established the mindset that makes
  threat hunting a natural approach rather than a
  reactive one.

## What I want to go deeper on
- Incident response specific to malware incidents —
  the triage, containment, and forensic analysis
  workflow when the threat is an active malware infection
- Zero Trust implementation at a technical level —
  how network microsegmentation, identity verification,
  and endpoint detection work together in practice
- Threat modeling — structured frameworks like STRIDE
  or MITRE ATT&CK for systematically identifying how
  an adversary might attack a specific environment
- Legal factors in malware analysis — computer fraud
  laws, responsible disclosure, and the legal boundaries
  around analyzing malware samples obtained from the wild
