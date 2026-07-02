# Lab 15 — Microsoft Entra ID User & Group Management

## Overview
Simulated a real employee onboarding and access management scenario using 
Microsoft Entra ID on Microsoft Azure. This lab mirrors real IT support tasks 
performed daily in corporate Microsoft environments.

**Platform:** Microsoft Azure — Microsoft Entra ID  
**Difficulty:** Beginner — Cloud Identity Management  
**Date:** July 2026  

---

## Scenario
Khumalo & Associates required two new employees to be onboarded into their 
Microsoft Entra ID environment. The IT team was responsible for creating user 
accounts, assigning department groups, and resolving an access issue that 
arose during the onboarding process.

**Users onboarded:**
- Thabo Mokoena — Finance Department
- Sipho Dlamini — Sales Department

---

## Ticket 001 — New User Onboarding

**Issue:** Two new employees required user accounts created before their start date.

**Steps Taken:**
1. Navigated to Microsoft Entra ID via portal.azure.com
2. Selected Users, then New User, then Create New User
3. Created user account for Thabo Mokoena (Finance Department)
4. Created user account for Sipho Dlamini (Sales Department)
5. Assigned temporary passwords and confirmed accounts were active

**Outcome:** Both user accounts successfully created and active in Entra ID.

### Screenshots

![User Creation Form](Screenshots/Screenshot%201.png)

![Screenshot Overview](Screenshots/Screenshot%201%20(user%20creating).png)

![Thabo Account Created](Screenshots/Thabo%20account.png)

![Sipho User Creating](Screenshots/Sipho%20user%20creating.png)

![Sipho Account Created](Screenshots/Sipho%20account.png)

---

## Ticket 002 — Group Creation & Member Assignment

**Issue:** Users needed to be assigned to their respective department security 
groups to enable correct access to resources.

**Steps Taken:**
1. Navigated to Groups in Microsoft Entra ID
2. Created Finance security group for Finance department access
3. Created Sales security group for Sales department access
4. Added Thabo Mokoena to the Finance group
5. Added Sipho Dlamini to the Sales group
6. Verified membership for both users

**Outcome:** Both groups created and users correctly assigned to their 
respective departments.

### Screenshots

![Finance Group Creating](Screenshots/Finance%20group%20(creating).png)

![Sales Group Creating](Screenshots/Sales%20group%20creating.png)

![Thabo Added to Finance Group](Screenshots/Thabo%20added%20to%20finance%20group.png)

![Sipho Added to Group](Screenshots/Sipho%20added%20to%20the%20group.png)

---

## Ticket 003 — Access Issue: Accidental Removal & Resolution

**Issue:** Thabo Mokoena was accidentally removed from the Finance group, 
resulting in loss of access to Finance department resources. Incident required 
immediate identification and resolution.

**Steps Taken:**
1. Identified that Thabo Mokoena had been removed from the Finance group
2. Documented the access gap with screenshot evidence
3. Navigated to Finance group in Microsoft Entra ID
4. Re-added Thabo Mokoena to the Finance group
5. Verified restored membership
6. Confirmed both users in correct groups as final verification

**Outcome:** Access fully restored. Both users confirmed in correct department 
groups. Incident resolved and documented.

### Screenshots

![Member Removed](Screenshots/member%20removed.png)

![Member Restored](Screenshots/Member%20restored.png)

![Final Finance Group Members](Screenshots/Final%20Member(finance).png)

![Final Sales Group Members](Screenshots/final%20member%20(sales).png)

---

## Skills Demonstrated
- Microsoft Azure portal navigation
- Microsoft Entra ID user account creation and management
- Security group creation and configuration
- Group membership assignment and administration
- Access issue identification, escalation, and resolution
- IT incident documentation following enterprise support standards

---

## Tools Used
- Microsoft Azure (portal.azure.com)
- Microsoft Entra ID (formerly Azure Active Directory)

---

## Part of My IT Lab Portfolio
This is Lab 15 in my ongoing IT support and infrastructure lab series.

- Phase 1 (Labs 1-9): Windows desktop support and troubleshooting
- Phase 2 (Labs 10-14): Windows Server, Active Directory, DNS, DHCP, Group Policy
- Lab 15: Microsoft Azure — Entra ID cloud identity management

