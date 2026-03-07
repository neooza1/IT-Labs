 Lab 2: Wrong IP Address (Subnet Mismatch)

**Scenario**  
User reported "I can't connect to the internet after trying to fix my network settings myself." This is a common helpdesk ticket when someone (or malware/VPN) manually sets a static IP that doesn't match the company network.

**Identified**  
Static IP configured with wrong subnet (Layer 3 error).

**Evaluated (OSI Bottom-Up)**  
- Layer 3: ipconfig showed incorrect static IP (192.168.1.100) with no gateway communication.

**Fixed**  
Reset adapter to DHCP:

**Confirmed**  
Restart VM → browser and ipconfig stable.

**Real-World Relevance**  
Happens daily in SA offices (banks, telcos, government). Quick fix prevents escalation and shows recruiters you can handle basic network troubleshooting.

**Tech Stack**  
- VirtualBox (Windows 10 VM)  
- Cmd commands (ipconfig, netsh)

**Screenshots**  
[Drag and drop your 5 screenshots here — GitHub will auto-upload them]  

![Baseline](https://github.com/user-attachments/assets/54121e51-8e76-48a5-9f78-949106d3bf32)

![Break Command](https://github.com/user-attachments/assets/7816e283-5bfb-4878-bb6a-2e093daf79fc)

![fixed  Result](https://github.com/user-attachments/assets/681cf95a-b63c-47f6-93c0-0158c854237f)


**Lab Note**  

[Notepad.txt](https://github.com/user-attachments/files/25813488/Notepad.txt)
Issue 2: Wrong IP Address 

Identified : Static IP set wrong ( Layer 3 user error).
Evaluated : ipconfig showed incorrect subnet, no connectivity.
Fixed : Reset to DHCP + release/renew.
Confirmed: Stable after restart.
Real-world: Users manually change IP or malware does it


