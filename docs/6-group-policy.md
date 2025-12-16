# Group Policy

<br>

## Objective
Apply group policies at the domain level and for individual OUs based on best practices

<br>

## Actions taken
- Domain-level GPO (baseline security):
  - Minimum password length - 12 characters
  - Password complexity requirements
  - Maximum password age - 60 days
  - Account lockout after 5 failed attempts
  - Lockout time 30 mins
  - Enforced Policy
- Domain-Controllers GPO:
  - Limited local server logon to domain admins only
  - Log logon events
  - Log directory service access
  - Enable Windows Defender Firewall
- Computer-level GPO:
  - Enable Windows Defender Firewall
  - Automatic updates
  - Disable local admin account
  - Screen lock after 15 mins inactivity

<br>

## Verification

Domain policy

![](/screenshots/domain_policy.png)

---

Domain Controller policy

![](/screenshots/DC_policy.png)

---

Computers policy

![](/screenshots/Computers_policy.png)
