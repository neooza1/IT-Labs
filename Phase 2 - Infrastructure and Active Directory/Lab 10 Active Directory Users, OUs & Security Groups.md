# Lab 10: Active Directory Users, OUs & Security Groups

## Scenario
A small company is onboarding new staff in different departments. IT needs to organize users into department OUs and assign security groups for access control.

## Identified
Active Directory needed a clean structure for departments, users, and access groups.

## Evaluated
Opened **Active Directory Users and Computers** and reviewed the existing domain structure in **lab.local** before making changes.

## Fixed
- Created two Organizational Units:
  - **Finance**
  - **IT**
- Created two user accounts:
  - **finance.user**
  - **it.user**
- Created two security groups:
  - **Finance_SG**
  - **IT_SG**
- Added each user to the correct security group:
  - **finance.user → Finance_SG**
  - **it.user → IT_SG**

## Confirmed
Users and groups were organized correctly inside their respective OUs, and group membership was verified in group properties.

## Real-World Relevance
This reflects a common systems administration task where IT organizes users by department and uses security groups for access control, delegated administration, and future file/share permissions.

## Tech Stack
- Windows Server 2022
- Active Directory Users and Computers
- VirtualBox

## Lessons Learned
- Organizational Units help keep Active Directory structured by department or business function.
- Security groups simplify access control and make future permissions easier to manage.
- Proper user and group organization is a core part of maintaining a scalable domain environment.

## Screenshots

### 1. Baseline (Active Directory before changes)
![Baseline ADUC](INSERT_IMAGE_LINK_HERE)

### 2. OUs and users created
![OUs and Users](INSERT_IMAGE_LINK_HERE)

### 3. Security groups created
![Security Groups](INSERT_IMAGE_LINK_HERE)

### 4. Group membership confirmed
![Group Membership](INSERT_IMAGE_LINK_HERE)

## Lab Note
This lab demonstrates foundational Active Directory administration by creating department OUs, user accounts, and security groups in a structured domain environment.