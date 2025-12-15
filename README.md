# Active Directory Help Desk Lab  
**Windows Server 2022 | Active Directory Domain Services | Group Policy**

## Overview
This project demonstrates hands-on experience with **Active Directory in a help desk–focused environment**, simulating common tasks performed in an enterprise or university-style domain.

The lab covers:
- Initial **domain setup and configuration**
- **User and computer management**
- **Common help desk workflows** (password resets, account unlocks, group membership changes)
- **Basic Group Policy usage**
- **Validation**

The emphasis is on **practical, entry-level IT support responsibilities**, with enough administrative exposure to show understanding of how AD works behind the scenes.

---

## Lab Environment

### Infrastructure
- **Hypervisor:** VMware
- **Server OS:** Windows Server 2022 (Evaluation)  
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

---

## Domain Setup (Administrative Tasks)

### 1. Install Active Directory Domain Services
- Installed the AD DS role on `DC01`
- Promoted the server to **Domain Controller**
- Created a new forest and domain

---

### 2(a). Organizational Unit (OU) Design
- Created OUs to simulate a University environment:
- lab_Users
  - Students
  - Faculty
  - IT staff
- lab_Computers
  - ClassroomPCs
  - StaffPCs

---

## User & Group Management

### 2(b). User Accounts and Computers
- Created user accounts for:
  - Students
  - Faculty
  - IT staff
- Configured:
  - Initial passwords
  - Forced password change at first login

---

### 3. Security Groups
- Created security groups for department-based access
- Added users to appropriate groups

---

## Client Configuration

### 4. Join Workstations to the Domain
- Joined `CLIENT01` to the domain using pre-staged computer
- Logged in using domain credentials

---

## Help Desk–Focused Tasks

### 5. Password Reset Workflow
Simulated a common ticket:
> “User forgot their password and is locked out.”

Actions performed:
- Reset user password in ADUC through helpdesk account on Client workstation using RSAT
- Forced password change at next login

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
- Technical documentation  

---

## Why This Lab Is Relevant to Help Desk Roles
This project reflects **real-world help desk responsibilities**, including:
- Account access issues
- Group membership changes
- Policy-related user problems

It also demonstrates understanding of how help desk work fits into **enterprise domain infrastructure**.

---
