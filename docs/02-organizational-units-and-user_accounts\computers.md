# Organizational Unit Design and User/Computer Creation

<br>

## Objective
Create basic OUs resembling University functions and populate them with user accounts and computers

<br>

## OU Population Strategy
Users are placed in role-based OUs to allow targeted Group Policy application.
Computers are placed in separate OUs to allow computer-specific policies.
Security groups will be stored in a dedicated Groups OU and used to control access.

<br>

## Steps performed
- Created Groups OU
- Created parent OU lab_Users containing sub-OUs:
  - Students
  - Faculty
  - IT_Staff
- Created parent OU lab_Computers containing sub-OUs:
  - Classroom_PCs
  - Staff_PCs
- Populated each sub-OU with user accounts and computers

<br>

## Validation

- Completed OUs inside the Active Directory Users and Computers tool tree structure

![](/screenshots/OU's_Design.png)
