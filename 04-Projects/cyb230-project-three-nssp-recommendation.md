# CYB 230 Project Three — Network System Security Plan Recommendation

**Course:** CYB 230 Operating Systems Security
**Format:** 2-3 page written report + cover page

## Scenario

Acted as security consultant for Helios Health Insurance, 
reviewing their Network System Security Plan (NSSP) and 
network diagram to identify deficiencies and recommend fixes. 
Selected **confidentiality** as the focus security objective 
given HIPAA/HITECH requirements for PHI.

## Deficiencies Identified

### Hardware — Unencrypted Laptop Hard Drives
Remote User laptops kept hard drives unencrypted "for faster 
performance." A lost or stolen laptop exposes all PHI on the 
device with no credential barrier — a reportable HIPAA breach.

**Fix:** Implement BitLocker full disk encryption with 
centralized key management via Active Directory. Modern 
encryption overhead is negligible (<5%), making the original 
performance justification invalid.

### Software — Telnet Used for Switch Administration
System administrators used Telnet (plaintext) to manage 
network switches, exposing admin credentials to interception.

**Fix:** Replace Telnet with SSH version 2, disable Telnet 
entirely, restrict SSH access to the System Administrators 
VLAN via ACLs.

## Key Lesson

Confidentiality risks exist at every layer — a single 
unencrypted laptop or a single legacy management protocol 
can undermine an otherwise reasonable security posture. 
Both deficiencies were "quiet" issues already documented in 
the org's own NSSP but never remediated, showing the gap 
between documentation and actual implementation.
