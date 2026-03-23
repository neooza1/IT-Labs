## Lab 14: DNS Configuration and Name Resolution (Windows Server 2022)



## Scenario:
A user was able to access a server using its IP address but failed to connect using the server name. This reflects a common real-world IT support issue where DNS name resolution is not properly configured or fails.


## Objective:
To configure DNS records on Windows Server 2022 and ensure that a Windows 10 client can resolve hostnames to IP addresses within a domain environment.

## Environment:
- VirtualBox
- Windows Server 2022 (Domain Controller + DNS Server)
- Windows 10 Pro (Domain Client)
- Domain: lab.local

Server Configuration:
- IP Address: 192.168.10.10
- Subnet Mask: 255.255.255.0
- Preferred DNS: 192.168.10.10

Client:
- Logged in as: LAB\testuser
- DNS configured automatically via DHCP


## Steps Performed:

1. Verified DNS Role
- Opened Server Manager → Tools → DNS
- Confirmed DNS Manager is accessible and operational

2. Checked Existing DNS Zone
- Navigated to Forward Lookup Zones
- Verified the domain zone (lab.local) exists

3. Created A Record (Host Record)
- Added a new host:
  - Name: server
  - IP Address: 192.168.10.10
- Enabled PTR record creation for reverse lookup

4. Cleared Client DNS Cache
- On Windows 10 client, executed:
  ipconfig /flushdns

5. Tested Name Resolution
- Used:
  ping server.lab.local
  nslookup server.lab.local

6. Verified Results
- Hostname successfully resolved to IP address
- Confirmed communication with server via hostname


## Challenges Encountered:

- Initial failure in hostname resolution
- DNS queries did not return expected results

Root Cause:
- DNS cache contained outdated records
- Missing or incorrect DNS record configuration

Resolution:
- Created correct A record in DNS Manager
- Flushed DNS cache on client machine
- Re-tested name resolution successfully


## Outcome:

The Windows 10 client successfully resolved the server hostname (server.lab.local) to its correct IP address (192.168.10.10). Connectivity using hostname was verified.


## Real-World Relevance:

DNS is a critical service in enterprise environments. Active Directory heavily relies on DNS for authentication, resource access, and system communication.

This lab demonstrates:
- DNS record management
- Name resolution troubleshooting
- Client-server communication using hostnames

Tools Used:
- Windows Server 2022
- Windows 10 Pro
- DNS Manager
- Command Prompt
- VirtualBox

## Screenshots
### 1. Baseline (DNS Manager)  
   <img width="1024" height="768" alt="Baseline DNS Manager" src="https://github.com/user-attachments/assets/7bd601f4-882c-46a3-ad85-717264907b7e" />


### 2. A record created in DNS Manager  
<img width="1024" height="768" alt="CreateRecord" src="https://github.com/user-attachments/assets/471affd7-5b61-4b3a-bf99-d09463f14fb4" />


### 3. Flush DNS + successful ping/nslookup  
   <img width="1918" height="943" alt="ping" src="https://github.com/user-attachments/assets/a4d539dd-7d56-439a-be0e-8e97bd59ce92" />

## Conclusion:

This lab provided hands-on experience in configuring DNS and resolving hostname-related issues. Understanding DNS is essential for diagnosing network and system access problems in real-world IT environments.



