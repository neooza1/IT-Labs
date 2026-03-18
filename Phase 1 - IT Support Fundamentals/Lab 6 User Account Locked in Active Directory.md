## Lab 6: User Account Locked in Active Directory

**Scenario**  
User calls helpdesk: “My account is locked, and I can’t log in.”  
Common enterprise ticket — account lockout after multiple failed password attempts in an Active Directory environment.

**Identified**  
- Domain user account `testuser` became locked after exceeding the configured failed sign-in threshold.

**Evaluated (Systems Level)**  
- Verified `testuser` existed in Active Directory Users and Computers.  
- Confirmed Windows 10 Pro client was joined to the `lab.local` domain.  
- Checked Group Policy and confirmed Account Lockout Policy was configured.  
- Confirmed the account lockout state in Active Directory Users and Computers.

**Fixed**  
- Opened Active Directory Users and Computers on the Domain Controller.  
- Located `testuser` in the `Users` container.  
- Unlocked the account in the user properties.

**Confirmed**  
- Logged in again from the Windows 10 Pro domain client using the correct credentials.  
- Verified successful domain authentication and restored access.

**Real-World Relevance**  
Common helpdesk and system administration issue in business environments using Active Directory.  
This lab demonstrates practical troubleshooting of user lockout, domain authentication, Group Policy enforcement, and account recovery.

**Tech Stack**  
- VirtualBox  
- Windows Server 2022 (Domain Controller)  
- Windows 10 Pro (Domain Client)  
- Active Directory Domain Services (AD DS)  
- Active Directory Users and Computers  
- Group Policy Management  

**Screenshots**  

1. User created in Active Directory  

<img width="1024" height="768" alt="UserCreated" src="https://github.com/user-attachments/assets/6100d01b-3ab3-4abe-8af9-e920f30d83bb" />



2. Client joined to domain (`lab.local`)  


<img width="1024" height="768" alt="Client joined" src="https://github.com/user-attachments/assets/079a4b52-a90f-42b3-a589-a969353e2e41" />


3. Baseline (domain user verified on client)  


<img width="1918" height="1078" alt="Baseline_DomainUserVerified" src="https://github.com/user-attachments/assets/39fc7697-a089-449d-bfca-266d5c9e4d0c" />


4. Lockout Policy configured in Group Policy  


<img width="1024" height="768" alt="LockOutPolicy" src="https://github.com/user-attachments/assets/3cc1d45a-d2c1-4689-8233-b30fd06a59a1" />


5. Break (account locked after failed sign-in attempts)  


<img width="1024" height="768" alt="Account locked" src="https://github.com/user-attachments/assets/7b0955d6-1277-46c0-ae0e-249343d6b4dc" />


6. Evaluate (lockout confirmed in Active Directory Users and Computers)  


<img width="1024" height="768" alt="Account locked out" src="https://github.com/user-attachments/assets/6b39f0db-b31f-4a38-b7e8-163ea09cd41e" />


7. Fixed (account unlocked in Active Directory)  


<img width="1024" height="768" alt="Account unlocked" src="https://github.com/user-attachments/assets/8b3f9f48-9c84-4937-b57f-63dbb4a448c3" />


8. Confirmed (successful login restored on Windows 10 Pro client)  


<img width="1024" height="768" alt="Account fixed" src="https://github.com/user-attachments/assets/357a2eeb-8622-4cc1-b43a-c489de9f682f" />


<img width="1024" height="768" alt="Account restored" src="https://github.com/user-attachments/assets/a8d57c08-92c5-4964-9e21-366d5c63f77e" />

*Lab Note*

 Lab 6: User Account Locked in Active Directory

**Scenario:**  
User could not log in because the domain account was locked.

**Identified:**  
`testuser` was locked after exceeding the account lockout threshold.

**Fixed:**  
Unlocked the account in Active Directory Users and Computers.

**Confirmed:**  
Successful login restored on the Windows 10 Pro domain client.

**Tools:**  
Windows Server 2022, Windows 10 Pro, AD DS, Group Policy, VirtualBoxading notepad.txt…]()


