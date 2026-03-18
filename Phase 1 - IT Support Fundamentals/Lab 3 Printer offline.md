# Lab 3: Printer Offline

**Scenario**  
User calls helpdesk: “My printer is offline, nothing prints.”  
This is a very common ticket in SA offices — user accidentally paused printing, driver glitched, or spooler service stopped.

**Identified**  
Printer paused/offline (most common user error).

**Evaluated (OSI & Systems Level)**  
- Layer 1–2: Physical connection and adapter OK.  
- Systems level: Printer status in Settings shows paused/offline; spooler service running but queue blocked.

**Fixed**  
- Resume printing via Printers & scanners settings.  
- If spooler issue, restart Print Spooler service (services.msc > Print Spooler > Restart).

**Confirmed**  
Restart VM → test print works. Stable.

**Real-World Relevance**  
Daily ticket in SA helpdesk . Quick resume/restart fix saves escalation time and shows recruiters you can handle common printer problems.

**Tech Stack**  
- VirtualBox (Windows 10 VM)  
- Windows Settings & services.msc

**Screenshots**  
 
1. Baseline (printer added + test page success)
   
![Baseline + printer added](https://github.com/user-attachments/assets/0ab3788b-5cf0-41ae-bfbb-9230b629f54b)

2. Break (printer paused + error message)

   ![Pinter stooped working](https://github.com/user-attachments/assets/3cb231d0-c0f5-4bbf-87d5-aff736d2fb3e)

   ![Printer not found](https://github.com/user-attachments/assets/ec5dcb96-e564-4f2f-950c-64cd81398a8a)

3. Evaluate
   
![Printer ready (fixed)](https://github.com/user-attachments/assets/4e067c1e-cfb6-452d-9b16-206b783c17dc)

   
4. Fixed (successful test page)
![printer fixed](https://github.com/user-attachments/assets/803aa176-0179-442d-b129-5c915547b1d2)



**Lab Note**  
[UploIssue 3: Printer Offline (Print Spooler Stopped)

Identified: Print Spooler service stopped (common cause of offline printers).
Evaluated: services.msc showed Print Spooler stopped.
Fixed: Restarted Print Spooler service.
Confirmed: Stable after restart.
Real-world: Very common helpdesk fix when pause doesn’t work or spooler crashes.ading Notepad.txt…]()


