# Lab 15 — Microsoft Entra ID User & Group Management

## Overview
Simulated a real onboarding and access management scenario using Microsoft Entra ID 
(Azure Active Directory) on Microsoft Azure. This lab mirrors real IT support tasks 
performed daily in corporate environments.

**Platform:** Microsoft Azure — Microsoft Entra ID  
**Difficulty:** Beginner  
**Date:** July 2026  

---

## Scenario
Khumalo & Associates required two new employees to be onboarded into their 
Microsoft Entra ID environment. The IT team was responsible for creating user 
accounts, assigning department groups, and resolving an access issue that 
arose during onboarding.

---

## Ticket 001 — New User Onboarding

**Issue:** Two new employees required user accounts before their start date.  
**Steps Taken:**  
1. Navigated to Microsoft Entra ID via portal.azure.com  
2. Selected Users, then New User, then Create New User  
3. Created Thabo Mokoena (Finance Department)  
4. Created Sipho Dlamini (Sales Department)  

**Outcome:** Both user accounts successfully created and active.  
**Screenshot:** [screenshot here]

---

## Ticket 002 — Group Assignment & Access Issue

**Issue:** Users needed to be assigned to department groups. 
Thabo Mokoena was accidentally removed from the Finance group, 
causing an access issue.  
**Steps Taken:**  
1. Created Finance and Sales groups in Entra ID  
2. Assigned Thabo to Finance, Sipho to Sales  
3. Simulated accidental removal of Thabo from Finance group  
4. Documented the resulting access gap  

**Outcome:** Access issue identified and logged for resolution.  
**Screenshot:** [screenshot here]

---

## Ticket 003 — Resolution & Verification

**Issue:** Thabo Mokoena lacked access to Finance group resources 
following accidental removal.  
**Steps Taken:**  
1. Located Thabo Mokoena in Entra ID Users  
2. Re-added to Finance group  
3. Verified group membership for both users  

**Outcome:** Access restored. Both users confirmed in correct groups.  
**Screenshot:** [screenshot here]

---

## Skills Demonstrated
- Microsoft Entra ID user creation and management
- Group creation and membership assignment
- Access issue identification and resolution
- IT documentation following enterprise standards

---

## Tools Used
- Microsoft Azure (portal.azure.com)
- Microsoft Entra ID (formerly Azure Active Directory)
