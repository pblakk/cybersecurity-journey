# CYB 230 Project Two — Server Configuration Verification Report

**Course:** CYB 230 Operating Systems Security
**Tools:** Windows Server 2012 R2 (old server), Windows Server 
2012 AD (new server)

## Scenario

Helios Health Insurance — scheduled hardware upgrade. 
Required backing up the old server and configuring the new 
server's Active Directory structure.

## Old Server Tasks

### Backup Configuration
Created Task Scheduler task "Server Backup" triggered on 
Event ID 4624 (Security log, successful logon), set to run 
`wbadmin.msc`.

### Event Viewer Custom View
Created custom view filtered for Event ID 4624 in the 
Security log. Named with student identifier and course 
section for audit traceability.

## New Server Configuration

### Organizational Unit
Created **OS Department** OU in Active Directory Users and 
Computers.

### New Users
Added three users to OS Department (using classmate names 
per assignment instructions): Jess McMurray, Daun Travis, 
PJ Ubom.

## Key Lesson

Event-triggered automation (Task Scheduler + Event Viewer) 
allows backup and audit processes to run without manual 
intervention — directly relevant to maintaining availability 
during infrastructure transitions without relying on someone 
remembering to run a backup manually.
