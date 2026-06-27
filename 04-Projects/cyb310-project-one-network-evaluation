# CYB 310 Project One — Network Evaluation Report

**Course:** CYB 310 Network Defense
**Tool:** GNS3
**Format:** 2-3 page written report

## Scenario

Evaluated a campus network (IT, Academic Affairs, Professor 
departments) for security deficiencies as part of a 
cybersecurity analyst interview exercise.

## Deficiencies Identified

### 1. Remote_Access_PC — Unrestricted Internal Access

Remote_Access_PC connected directly to Edge_Firewall with 
unrestricted access to the entire internal network instead 
of being limited to Remote_Admin_FTP_Server only.

**Fix:** Restrict firewall ACLs to permit only 
Remote_Access_PC → Remote_Admin_FTP_Server traffic. Place 
the FTP server in a dedicated DMZ so a compromised server 
cannot pivot into the internal network.

### 2. No VLAN Segmentation Between Departments

IT, Academic Affairs, and Professor PCs shared a flat 
network with no VLAN segmentation, allowing cross-department 
authentication and lateral movement.

**Fix:** Implement VLAN segmentation (IT=10, Academic 
Affairs=20, Professors=30) with VLAN ACLs on the Campus 
Router, combined with Active Directory "Allow log on 
locally" restrictions per department.

## Key Lesson

Least privilege must be enforced at both the network layer 
(VLANs/ACLs) and the identity layer (AD login restrictions) — 
either alone is insufficient defense in depth.
