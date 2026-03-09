# Lab 5: Remote Desktop Simulation (AnyDesk Connection Fail)

**Scenario**  
User calls helpdesk: “I can't connect remotely to my computer.”  
Common ticket — firewall block, wrong ID, or remote service disabled.

**Identified**  
AnyDesk service stopped (common issue or user error).

**Evaluated (Systems Level)**  
- services.msc showed AnyDesk Service status “Stopped”.

**Fixed**  
- Right-click AnyDesk Service → Start.

**Confirmed**  
Restart VM → test connect stable.

**Real-World Relevance**  
Frequent ticket in SA helpdesk . Quick service restart fixes remote access issues and shows recruiters you can handle common remote tool problems.

**Tech Stack**  
- VirtualBox (Windows 10 VM)  
- AnyDesk  
- services.msc

**Screenshots**  

1. Baseline (successful remote session)


<img width="1917" height="1076" alt="Baseline" src="https://github.com/user-attachments/assets/02cb427a-b55b-4781-9292-337b00e9e48d" />

3. Break (service stopped + connection error)


<img width="1024" height="768" alt="Service stopped" src="https://github.com/user-attachments/assets/1c8f203b-3909-4de1-9d9b-0ffa3d895723" />


<img width="1793" height="1003" alt="Issue error" src="https://github.com/user-attachments/assets/f979e548-751f-42a2-80a1-430357109e86" />



4. Evaluate (stopped service in services.msc)  

<img width="1024" height="768" alt="Serive stopped evaluate" src="https://github.com/user-attachments/assets/18021785-debb-407b-8224-41f3bfc60cc6" />


5. Fixed (service started + successful session)  


<img width="1024" height="768" alt="Service fixed" src="https://github.com/user-attachments/assets/582c0721-5cfc-4074-ad76-59e9b507166c" />

<img width="1918" height="1072" alt="Service works" src="https://github.com/user-attachments/assets/a93de402-d0f2-44b1-9340-156435a0dd8f" />



**Lab Note**  
[Lab 5  Remote Desktop Simulation (Anydesk).md](https://github.com/user-attachments/files/25829278/Lab.5.Remote.Desktop.Simulation.Anydesk.md)


