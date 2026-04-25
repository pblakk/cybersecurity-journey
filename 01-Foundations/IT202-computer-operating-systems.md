# IT 202 — Computer Operating Systems

Completed: December 2025

## Topics covered
- Operating system selection and planning — recommending
  OS choices for business scenarios based on user needs,
  software compatibility, and hardware capabilities
- Site surveys — assessing IT infrastructure, evaluating
  OS versions, and identifying security vulnerabilities
  across organizational systems
- Windows, Linux, and macOS features — exploring how
  each OS manages resources, users, and permissions
- Virtualization — understanding virtual operating systems
  and their role in supporting remote work and sandboxing
- OS troubleshooting — diagnosing and resolving common
  access and system issues in organizational environments
- Knowledge base documentation — creating structured
  help desk documentation for repeatable problem resolution
- Infrastructure assessment — evaluating existing systems
  for vulnerabilities, compatibility, and upgrade needs

## Projects completed

### Project 1 — Site survey and proposal
Created a detailed assessment of operating systems across
departments to identify security vulnerabilities and
propose upgrades. Evaluated current OS versions against
organizational requirements and security best practices.

### Project 2 — Troubleshooting case studies
Developed a knowledge base for help desk scenarios
covering common user access problems. Created structured
documentation for repeatable diagnosis and resolution
of system issues.

### OS recommendation
Evaluated Windows 11 vs Linux for company-wide deployment.
Balanced cost, compatibility, security, and administrative
overhead to produce a justified recommendation.

## What I understand now that I didn't before
- Operating system selection is a security decision.
  Choosing an OS that is end-of-life, unsupported, or
  incompatible with security tooling creates vulnerabilities
  that cannot be patched away. The decision made at
  deployment time has security consequences for years.
- Site surveys reveal the gap between what IT thinks
  is deployed and what is actually running. Undocumented
  systems, outdated OS versions, and unsupported software
  are exactly the footholds malware exploits. You cannot
  defend what you do not know exists.
- Linux is not just a server OS. Understanding Linux
  features and administration is essential for malware
  analysis because most analysis tools — Volatility,
  REMnux, many forensics utilities — run on Linux.
  This course started building Linux familiarity that
  the roadmap develops further.
- Virtualization is a security tool as much as an
  administrative one. Understanding how virtual machines
  work at the OS level explains why malware analysts
  use them for dynamic analysis and why some malware
  specifically detects and behaves differently inside
  virtual environments.
- Troubleshooting methodology is transferable. The
  systematic approach to diagnosing OS problems —
  identify symptoms, isolate variables, test solutions —
  is the same methodology used in malware analysis
  when working through unknown behavior.

## Connection to malware analysis
- **Windows internals knowledge is foundational to
  malware analysis.** Almost all malware targets Windows.
  Understanding how Windows manages processes, memory,
  files, and registry at an OS level is the substrate
  that every malware analysis technique builds on.
- **Linux familiarity enables the analysis toolchain.**
  REMnux — the standard malware analysis Linux
  distribution — requires Linux comfort to use
  effectively. IT 202 started building that comfort.
- **Virtualization connects directly to dynamic analysis
  lab setup.** Understanding how virtual machines work
  at the OS level explains how to configure isolated
  analysis environments and why snapshot and revert
  functionality is essential for safe malware execution.
- **Site survey methodology connects to incident response
  scoping.** When malware is detected in an environment
  the first question is scope — what systems are affected?
  The site survey approach from IT 202 is the same
  systematic inventory process used to answer that
  question during an incident.
- **OS vulnerability identification connects to malware
  targeting.** Malware exploits specific OS versions,
  unpatched vulnerabilities, and misconfigured features.
  Understanding how to identify those weaknesses from
  a defender's perspective makes it easier to recognize
  what malware is targeting when you analyze it.

## What I want to go deeper on
- Windows internals at a deep level — processes, threads,
  memory management, registry structure, and how the
  Windows API works. This is the foundation for
  understanding what malware does to a Windows system
  at a technical level.
- Linux administration beyond basics — file permissions,
  process management, and shell scripting fluency needed
  to use REMnux and other analysis tools effectively.
  Linux Basics for Hackers on the reading list addresses
  this directly.
- Malware-specific virtualization topics — how malware
  detects virtual environments and attempts to evade
  analysis by behaving differently inside a VM.
  Covered in Evasive Malware in Phase 3.
- Memory management at the OS level — how the OS
  allocates and manages memory, which is the foundation
  for understanding process injection, shellcode
  execution, and memory forensics in later phases.
