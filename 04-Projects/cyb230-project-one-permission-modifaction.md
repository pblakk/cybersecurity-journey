# CYB 230 Project One — Permission Modification

**Course:** CYB 230 Operating Systems Security
**Tools:** Windows Server (AD/GPO), Linux

## Scenario

Helios Health Insurance — Pat Smith promoted from Finance to 
HR Manager. Required updating file permissions, password 
policy, and creating a Linux admin account.

## Tasks Completed

### Windows — File Permissions
- Removed Pat from Finance folder permissions
- Added Pat to HR folder with Full Control

### Windows — GPO Password Policy
Configured to meet Helios admin requirements:
- Minimum length: 10 characters
- Complexity: Enabled
- Password history: 3 passwords remembered
- Maximum age: 180 days
- Enabled "User must change password at next logon" via 
  Active Directory Users and Computers (dsa.msc)

Verified enforcement by attempting a non-compliant password 
change — received error: *"The password does not meet the 
password policy requirements."*

### Linux — New Admin User
Created HR admin user for Pat on Ubuntu LTS using `adduser`, 
verified login with `su - patsmith`.

## Key Lesson

Password policy enforcement requires both the GPO 
configuration AND a forced password reset trigger — 
configuring the policy alone doesn't retroactively force 
existing users to comply until their next required change.
