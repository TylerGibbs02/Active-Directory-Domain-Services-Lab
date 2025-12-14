# Active Directory Help Desk Lab  
**Windows Server 2022 | Active Directory Domain Services | Group Policy**

## Overview
This project demonstrates hands-on experience with **Active Directory in a help desk–focused environment**, simulating common tasks performed in an enterprise or university-style domain.

The lab covers:
- Initial **domain setup and configuration**
- **User and computer management**
- **Common help desk workflows** (password resets, account unlocks, group membership changes)
- **Basic Group Policy usage**
- **Troubleshooting and validation**

The emphasis is on **practical, entry-level IT support responsibilities**, with enough administrative exposure to show understanding of how AD works behind the scenes.

---

## Lab Environment

### Infrastructure
- **Hypervisor:** VMware
- **Server OS:** Windows Server 2022 Datacenter Graphical (Evaluation)  
- **Client OS:** Windows 11  
- **Domain Name:** `lab.local`

### Virtual Machines
| VM Name | Role |
|------|------|
| DC01 | Domain Controller (AD DS, DNS) |
| CLIENT01 | Domain-joined workstation |

---

## Objectives
- Build a functional Active Directory domain from scratch  
- Perform **daily help desk tasks using ADUC**  
- Apply **basic security and organizational best practices**  
- Document procedures clearly for repeatability  

---

## Domain Setup (Administrative Tasks)

### 1. Install Active Directory Domain Services
- Installed the AD DS role on `DC01`
- Promoted the server to **Domain Controller**
- Created a new forest and domain

**Help Desk Relevance:**  
Understanding domain creation helps explain authentication behavior and common login issues.

---

### 2. DNS Verification
- Verified DNS was installed automatically
- Confirmed domain name resolution from clients using `nslookup`
- Validated SRV records

---

### 3. Organizational Unit (OU) Design
Created OUs to simulate a real environment:



## User & Group Management

### 4. User Account Creation
- Created user accounts for:
  - Students
  - Faculty
  - IT staff
- Configured:
  - Initial passwords
  - Forced password change at first login

---

### 5. Security Groups
- Created security groups for:
  - Printer access
  - Shared folders
  - Department-based access
- Added and removed users from groups

**Help Desk Relevance:**  
Group membership updates are one of the most common access-related tickets.

---

## Client Configuration

### 6. Join Workstations to the Domain
- Joined `CLIENT01` to the domain
- Verified computer account creation in AD
- Logged in using domain credentials

---

## Help Desk–Focused Tasks

### 7. Password Reset Workflow
Simulated a common ticket:
> “User forgot their password and is locked out.”

Actions performed:
- Reset user password in ADUC
- Forced password change at next login

---

### 8. Account Lockout & Unlock
- Intentionally locked a user account
- Identified lockout status in ADUC
- Unlocked account and verified access

---

### 9. Enable / Disable User Accounts
- Disabled accounts for 'terminated users'
- Re-enabled accounts
- Verified login behavior from client machines

---

### 10. Group Policy Basics
Applied simple Group Policies:
- Password complexity enforcement
- Disabled Control Panel for student users
- Mapped a network drive

Linked GPOs at:
- Domain level
- OU level

Validated using:
- `gpresult /r`
- `rsop.msc`

---

## Troubleshooting Scenarios

### 11. Login Failure Diagnosis
Simulated and resolved:
- Incorrect password errors
- Disabled account logins
- Missing group access issues

Tools used:
- Active Directory Users and Computers
- Event Viewer
- Client-side error messages

---

### 12. DNS / Authentication Issue
- Misconfigured client DNS settings
- Identified domain login failure
- Corrected DNS configuration
- Verified restored domain connectivity

---

## Documentation & Validation
- Screenshots of:
  - ADUC structure
  - User and group properties
  - GPO links
- Command outputs:
  - `ipconfig /all`
  - `gpresult /r`
- Step-by-step documentation for each task

---

## Skills Demonstrated
- Active Directory fundamentals  
- User and computer account management  
- Password resets and account unlocks  
- Group-based access control  
- Basic Group Policy administration  
- Windows domain troubleshooting  
- Technical documentation  

---

## Why This Lab Is Relevant to Help Desk Roles
This project reflects **real-world help desk responsibilities**, including:
- Account access issues
- Login troubleshooting
- Group membership changes
- Policy-related user problems

It also demonstrates understanding of how help desk work fits into **enterprise domain infrastructure**.

---
