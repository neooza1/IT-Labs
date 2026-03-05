# IT Support Labs

Hands-on troubleshooting labs to build entry-level IT support skills. Simulates real-world helpdesk tickets like connectivity issues, using VirtualBox for Windows environments. Focus on OSI model diagnostics, fixes, and documentation for SA roles.

## Lab 1: No Internet Connectivity

Simulated common user ticket: "No Wi-Fi" caused by disabled adapter (e.g., accidental toggle or config error). Diagnosed bottom-up OSI, fixed in 5 mins.

## Process
- Identified: User report "no internet" — reproduced error.
- Evaluated: OSI Layer 1 (physical connection in VirtualBox enabled?); Layer 2 (adapter disabled); Layer 3 (no IP from ipconfig).
- Fixed: Enabled adapter, ipconfig /release /renew to get DHCP IP.
- Confirmed: Restart VM, test browser — stable.

## Real-World Relevance
- 30% helpdesk calls are connectivity (Layer 1/2/3 user errors, e.g., Wi-Fi switch off); fixes like this prevent escalation in SA telcos/banks.
- Builds troubleshooting for CCNA certs — recruiters test this in interviews (e.g., "Explain no IP fix").

## Tech Stack
- VirtualBox for VM
- Windows 10 for OS
- Cmd for ipconfig/netsh commands

## Challenges & Solutions
- Challenge: No IP after enable — Solution: /release /renew to refresh DHCP.
- Challenge: VM network — Solution: Checked VirtualBox settings (Layer 1).

## Screenshots
<img width="1280" height="720" alt="Baseline + error page" src="https://github.com/user-attachments/assets/ca2d6f2d-aabc-4065-9e5e-0a6706af2ffd" />

<img width="1280" height="720" alt="Disabled adapter + No IP" src="https://github.com/user-attachments/assets/68be63fe-3020-4abd-8f2e-a0cbc3c74392" />

<img width="1280" height="720" alt="Enabled adapter + Fixed IP" src="https://github.com/user-attachments/assets/0c950e2a-afc7-4ac8-8fd1-3640a61f4ddd" />

<img width="1024" height="768" alt="Fixed browser" src="https://github.com/user-attachments/assets/8d4695f6-024c-485c-9fc4-96bbd57920d0" />

[Lab note.txt](https://github.com/user-attachments/files/25779994/Lab.note.txt)
Full Troubleshooting Note (from my lab log)
Identified: Disabled adapter (Layer 2 user error, e.g. accidental toggle). 
Evaluated: OSI bottom-up — Layer 1 checked in VirtualBox, Layer 2 disabled, Layer 3 no IP from ipconfig. 
Fixed: Enabled adapter + ipconfig /release /renew. 
Confirmed: Restart VM, browser stable. 
Time: 5 mins. Real-world: Common helpdesk ticket 


## Note


Built to demonstrate systematic problem-solving for helpdesk roles; open to feedback.
