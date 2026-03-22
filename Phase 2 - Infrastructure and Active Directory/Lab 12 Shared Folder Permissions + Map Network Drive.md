# Lab 12: Shared Folder Permissions + Map Network Drive

## Scenario
A company needs a shared **Finance department folder** on the server so authorized users can access common files from their domain-joined workstations. IT must configure the shared folder, apply group-based permissions, and map it as a network drive for the Finance user.

## Identified
Finance users needed secure access to a department shared folder with both **read and write permissions**.

## Evaluated
- Confirmed **finance.user** existed in Active Directory
- Confirmed **Finance_Users** security group existed
- Verified **finance.user** was a member of **Finance_Users**
- Verified the **Windows 10 Pro** client was joined to the **lab.local** domain
- Confirmed both VMs were connected to the same **Internal Network** in VirtualBox

## Fixed
- Created **C:\FinanceShare** on the Windows Server 2022 domain controller
- Added a test file named **finance-test.txt** inside the folder
- Enabled **Advanced Sharing** and shared the folder as **FinanceShare**
- Removed **Everyone** from Share permissions
- Added **Finance_Users** with **Read** and **Change** permissions
- Added **Finance_Users** to NTFS permissions on the **Security** tab with **Modify**, **Read**, and **Write** access
- Signed in to the Windows 10 Pro client as **LAB\finance.user**
- Accessed the share from the client using **\\SERVERNAME\FinanceShare**
- Mapped the shared folder as drive **F:**
- Created a second test file from the client to confirm write access

## Confirmed
The Finance shared folder opened successfully from the Windows 10 Pro domain client, was mapped as a network drive, and **finance.user** was able to read existing files and create a new file inside the share.

## Lessons Learned
- Both **Share permissions** and **NTFS permissions** must be configured correctly for access to work
- Security groups provide cleaner access control than assigning permissions directly to individual users
- Mapped network drives make department shares easier for end users to access
- File sharing in a domain environment requires both **server-side setup** and **client-side validation**

## Real-World Relevance
This reflects a common IT support and systems administration task where shared department folders are created on a server, access is controlled through **Active Directory groups**, and the share is mapped to user workstations for easier access.

This is a common office IT scenario in environments where departments like Finance, HR, and Operations use centralized shared drives for collaboration.

## Tech Stack
- Windows Server 2022
- Windows 10 Pro
- Active Directory Domain Services (AD DS)
- File Explorer / Shared Folders
- VirtualBox

## Screenshots

### 1. Server-side Share and NTFS permissions configured for Finance_Users
![Server Share and NTFS Permissions](INSERT_IMAGE_LINK_HERE)

### 2. finance.user accesses the FinanceShare folder from the Windows 10 domain client
![Client Access to Share](INSERT_IMAGE_LINK_HERE)

### 3. FinanceShare mapped as a network drive (F:)
![Mapped Network Drive](INSERT_IMAGE_LINK_HERE)

### 4. Confirmed read and write access from the mapped drive
![Confirmed Read Write Access](INSERT_IMAGE_LINK_HERE)

## Lab Note
This lab demonstrates practical **file sharing and access control** in a domain environment by creating a shared folder on a Windows Server, assigning both **Share** and **NTFS** permissions to an Active Directory security group, validating access from a domain-joined Windows 10 client, and mapping the share as a network drive for end-user usability.