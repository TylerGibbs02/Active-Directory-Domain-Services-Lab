# Password Reset Workflow

<br>

##Objective
Follow a common scenario of a domain user requesting a password reset

<br>

## Scenario
A Faculty user has forgotten their password and has been locked out of their account. After confirming their identity the helpdesk is tasked with forcing a password reset.

<br>

## Steps taken
- Delegated helpdesk account permission to reset user passwords and force password change at next logon
- Accessed helpdesk user account
- Opened RSAT: Users and Computers tool
- Located the correct Faculty user
- Reset password to a temporary password to be communicated to the faculty member and check 'force password change at next logon'
- Logged into Client VM through the faculty account and changed to a permanent password

<br>

## Validation

Password reset and force reset at logon through RSAT: Users and Computers tool

![](/screenshots/reset_password.png)

Resetting password at next logon

![](/screenshots/next_logon_reset.png)
