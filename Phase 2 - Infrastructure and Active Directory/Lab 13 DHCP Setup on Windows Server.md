## Lab 13: DHCP Configuration and Client IP Lease (Windows Server 2022)



## Scenario:
A Windows 10 Pro client in a domain environment was unable to receive an IP address automatically. This simulated a common real-world infrastructure issue where devices fail to obtain a DHCP lease, affecting connectivity and productivity.



## Objective:

To configure a DHCP Server on Windows Server 2022 and ensure that a domain-joined Windows 10 client can successfully obtain an IP address automatically.


## Environment:
- VirtualBox
- Windows Server 2022 (Domain Controller)
- Windows 10 Pro (Domain Client)
- Domain: lab.local

Server Configuration:
- IP Address: 192.168.10.10
- Subnet Mask: 255.255.255.0
- Preferred DNS: 192.168.10.10

Client:
- Logged in as: LAB\testuser
- Configured to obtain IP and DNS automatically



## Steps Performed:

1. Verified Client Network State
- Ran ipconfig /all on Windows 10 client
- Observed current IP configuration before DHCP setup

2. Configured Client for DHCP
- Set IPv4 settings to:
  - Obtain IP address automatically
  - Obtain DNS server automatically

3. Installed DHCP Server Role
- Used Server Manager → Add Roles and Features
- Selected DHCP Server and installed required features

4. Completed Post-Installation Configuration
- Authorized DHCP in Active Directory
- Completed setup using Server Manager notification

5. Created DHCP Scope
- Scope Name: Lab Scope
- Network Range: 192.168.10.100 – 192.168.10.150
- Subnet Mask: 255.255.255.0
- DNS Server: 192.168.10.10
- Domain Name: lab.local
- Scope activated

6. Renewed Client IP Address
- Executed:
  ipconfig /release
  ipconfig /renew

7. Verified DHCP Lease
- Confirmed:
  - DHCP Enabled: Yes
  - IP address assigned within scope range
  - DNS server correctly set to 192.168.10.10

8. Tested Connectivity
- Successfully pinged the server (192.168.10.10)
- Verified name resolution using nslookup



## Challenges Encountered:

- DHCP lease failed during initial ipconfig /renew attempt
- Client could not contact DHCP server

Root Cause:
- Network adapter mismatch (NAT vs Internal Network)
- DHCP scope not properly active / configured

Resolution:
- Ensured both VMs were on the same Internal Network in VirtualBox
- Activated DHCP scope
- Restarted DHCP service where necessary
- Re-ran ipconfig /release and ipconfig /renew



## Outcome:

The Windows 10 client successfully received an IP address from the DHCP server. Network connectivity and DNS resolution were confirmed.


## Tools Used:
- Windows Server 2022
- Windows 10 Pro
- DHCP Server
- Server Manager
- Command Prompt
- VirtualBox

  ## Screenshots
  ### 1. Baseline (client IP details before DHCP)

  <img width="1024" height="768" alt="Baseline" src="https://github.com/user-attachments/assets/990ca9f9-17a9-40cb-982e-a2450c005c80" />


  ### 2. Client adapter set to obtain IP automatically

  <img width="1024" height="768" alt="Lab13 clientDHCP" src="https://github.com/user-attachments/assets/599a2f4d-8148-493b-ad68-51bf0c43572c" />


 
  ### 3. DHCP role installed on Windows Server

  <img width="1024" height="768" alt="DHCProle" src="https://github.com/user-attachments/assets/2cea6afc-5ef2-4491-a6ee-e46044d9c8e1" />

	### 4. DHCP post-install configuration completed

   <img width="1024" height="768" alt="Configiration Complete" src="https://github.com/user-attachments/assets/170cac85-c8a1-4d40-9cc3-072bc54d6d60" />

	### 5. DHCP scope created and activated

  <img width="1024" height="768" alt="Scope created" src="https://github.com/user-attachments/assets/4c2a8ebc-0676-4d6b-bf64-69d66b75d833" />

	### 6. Client successfully received DHCP lease

  <img width="1024" height="768" alt="Lease success" src="https://github.com/user-attachments/assets/3cda6b5d-8b1d-488b-ac7d-ffa1464e6709" />

	### 7. Connectivity confirmed (ping / optional nslookup)
<img width="1024" height="768" alt="Confirmed" src="https://github.com/user-attachments/assets/f9976dc5-ca1d-4bd6-9dd1-e171dee0c154" />


## Conclusion:

This lab strengthened practical understanding of DHCP configuration and troubleshooting in a Windows Server environment. It highlights the importance of proper network setup and service configuration in enterprise environments.

