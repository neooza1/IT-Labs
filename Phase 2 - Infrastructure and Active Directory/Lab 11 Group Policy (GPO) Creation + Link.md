# Lab 11: Group Policy (GPO) Creation + Link

## Scenario
A company wants to restrict Finance department users from accessing **Control Panel** to prevent unauthorized system changes. IT applies a **Group Policy Object (GPO)** to the **Finance OU** so the restriction is managed centrally in the domain.

## Identified
Finance users needed a centralized restriction to prevent access to **Control Panel and PC settings**.

## Evaluated
- Confirmed the **Finance OU** existed in Active Directory
- Confirmed **finance.user** was created and placed inside the **Finance OU**
- Verified the **Windows 10 Pro** client was joined to the **lab.local** domain
- Tested baseline access and confirmed **Control Panel** opened normally before policy was applied

## Fixed
- Opened **Group Policy Management** on the domain controller
- Created a new GPO named **Finance_ControlPanel_Restriction**
- Linked the GPO to the **Finance OU**
- Enabled **"Prohibit access to Control Panel and PC settings"**
- Ran **gpupdate /force** on the Windows 10 domain client
- Signed back in as **LAB\finance.user**

## Confirmed
Control Panel access was blocked for **finance.user** after Group Policy was applied.

## Challenge & Fix
During testing, the Windows 10 domain client initially showed that the domain was not available because the VM was still using **NAT** instead of the same **Internal Network** as the domain controller.

### Cause
The Windows 10 VM could not reliably communicate with the **Windows Server 2022** domain controller during sign-in.

### Fix
- Shut down both VMs
- Changed both the **Windows Server 2022** VM and the **Windows 10 Pro** VM to the same **Internal Network** in VirtualBox
- Started the **server first**, then the **client**
- Verified domain access before continuing the GPO test

This restored domain authentication and allowed **finance.user** to sign in successfully.

## Lessons Learned
- Group Policy provides centralized control of user and computer settings in a domain environment
- GPOs must be linked to the correct **OU** to apply to the intended users
- User-based policies often require **gpupdate /force** and re-login
- Domain authentication depends on correct VM networking and domain controller availability

## Real-World Relevance
This reflects a common systems administration task where IT restricts access to system settings for specific departments to:
- reduce risk
- standardize workstation configurations
- prevent unauthorized user changes
- support controlled end-user environments

The network issue during testing also mirrors a real infrastructure support scenario where incorrect VM configuration can break domain authentication.

## Tech Stack
- Windows Server 2022
- Windows 10 Pro
- Active Directory Domain Services (AD DS)
- Group Policy Management
- VirtualBox

## Screenshots

### 1. Baseline (finance.user logged in, Control Panel accessible before policy)
![Baseline Control Panel Access](INSERT_IMAGE_LINK_HERE)

### 2. GPO created and linked to Finance OU
![GPO Linked to Finance OU](INSERT_IMAGE_LINK_HERE)

### 3. Policy enabled in Group Policy Editor
![Policy Enabled](INSERT_IMAGE_LINK_HERE)

### 4. Control Panel blocked after policy application
![Control Panel Blocked](INSERT_IMAGE_LINK_HERE)

## Lab Note
This lab demonstrates practical **Group Policy administration** by creating and linking a user-based GPO to a department OU, validating the restriction on a domain-joined Windows 10 client, and troubleshooting a real domain connectivity issue caused by incorrect VM network settings.