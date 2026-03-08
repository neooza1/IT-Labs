# Lab 4: Sound Driver Error

**Scenario**  
User calls helpdesk: “No sound from speakers or headphones.”  
This is a very common ticket in SA offices — user accidentally disabled the audio device, driver glitched, or malware changed settings.

**Identified**  
Audio playback device disabled (common user error or driver issue).

**Evaluated (Systems Level)**  
- Sound settings (Playback tab) showed default device status “Disabled”.

**Fixed**  
- Right-click device in Sounds > Playback > Enable.
- Test sound → works.

**Confirmed**  
Restart VM → test sound stable.

**Real-World Relevance**  
Daily ticket in helpdesk roles . Quick enable fix saves escalation time and shows recruiters you can handle common device driver issues.

**Tech Stack**  
- VirtualBox (Windows 10 VM)  
- Windows Sounds settings

**Screenshots**  
[Drag and drop your 5 screenshots here — GitHub auto-uploads them]  
1. Baseline (sound working, audio icon active) 

<img width="1024" height="768" alt="sound test baseline" src="https://github.com/user-attachments/assets/aa11a893-b43b-46c3-a48b-bbeffb25ecd9" />

2. Break (device disabled, no audio)  

<img width="1024" height="768" alt="No sound" src="https://github.com/user-attachments/assets/050249a5-e21e-4d68-8303-3f132a1d61cb" />

3. Evaluate (device status “Disabled” in Playback tab) 

<img width="1024" height="768" alt="Sound disabled (Evaluate)" src="https://github.com/user-attachments/assets/16f6f8ac-55a3-42d6-9898-95face3efefa" />

4. Fixed (device enabled, sound playing)  

<img width="1024" height="768" alt="Sound working" src="https://github.com/user-attachments/assets/ac7733bf-aaf3-4446-9a06-6c02a75b9883" />

*Lab Note*

[Notepad.txt](https://github.com/user-attachments/files/25820432/Notepad.txt)
Issue 4: Sound Driver Error

Identified: Audio device disabled (common user error or driver issue).
Evaluated: Device status “Disabled” in Sounds settings.
Fixed: Enabled device.
Confirmed: Stable after restart.
Real-world: Frequent helpdesk ticket — users disable audio accidentally or driver glitches.
  





**Lab Note**  
[Copy-paste your Notepad text here]
