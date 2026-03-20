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

<img width="1024" height="768" alt="Baseline" src="https://github.com/user-attachments/assets/8adda31c-9ab1-4444-a0e1-a35c7afa7805" />


### 2. OUs and users created

![OUs + Users expanded](https://github.com/user-attachments/assets/845ebf5d-0b4d-4ef3-b297-20d2ca6e4b8c)


### 3. Security groups created

<img width="1024" height="768" alt="Lab 10 IT Security Group" src="https://github.com/user-attachments/assets/e86c1e11-7df8-4b99-87de-13591aebcddb" />


### 4. Group membership confirmed

<img width="1024" height="768" alt="IT user listed" src="https://github.com/user-attachments/assets/812e22fe-a037-4648-8e87-c9907e79c56f" />


## Lab Note
This lab demonstrates foundational Active Directory administration by creating department OUs, user accounts, and security groups in a structured domain environment.
[Notepad for Lab 10.txt](https://github.com/user-attachments/files/26132993/Notepad.for.Lab.10.txt)

