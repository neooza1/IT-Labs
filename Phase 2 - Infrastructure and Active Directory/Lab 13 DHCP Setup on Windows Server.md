Lab 13: DHCP Configuration and Client IP Lease (Windows Server 2022)

------------------------------------------------------------

Scenario:
A Windows 10 Pro client in a domain environment was unable to receive an IP address automatically. This simulated a common real-world infrastructure issue where devices fail to obtain a DHCP lease, affecting connectivity and productivity.

------------------------------------------------------------

Objective:
To configure a DHCP Server on Windows Server 2022 and ensure that a domain-joined Windows 10 client can successfully obtain an IP address automatically.

------------------------------------------------------------

Environment:
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

------------------------------------------------------------

Steps Performed:

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

------------------------------------------------------------

Challenges Encountered:

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

------------------------------------------------------------

Outcome:

The Windows 10 client successfully received an IP address from the DHCP server. Network connectivity and DNS resolution were confirmed.

------------------------------------------------------------

Real-World Relevance:

This lab demonstrates a common IT support and infrastructure task involving:
- DHCP server deployment
- IP address management
- Network troubleshooting
- Client-server communication validation

These are critical skills for:
- IT Support Specialist
- Junior Systems Administrator
- Infrastructure Support Technician
- Network Support Roles

------------------------------------------------------------

Tools Used:
- Windows Server 2022
- Windows 10 Pro
- DHCP Server
- Server Manager
- Command Prompt
- VirtualBox

------------------------------------------------------------

Conclusion:

This lab strengthened practical understanding of DHCP configuration and troubleshooting in a Windows Server environment. It highlights the importance of proper network setup and service configuration in enterprise environments.

------------------------------------------------------------