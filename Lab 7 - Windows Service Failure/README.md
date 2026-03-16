# Lab 7: Windows Service Failure (Windows Update Service Stopped)

## Scenario
User reported: **"Windows Update is not working."**  
This is a realistic desktop support issue where a critical Windows service is stopped, preventing the system from checking for updates.

## Identified
The **Windows Update** service was stopped, causing update checks to fail.

## Evaluated (Systems Level)
- Opened `services.msc`
- Verified that the **Windows Update** service was not running
- Confirmed the issue by testing Windows Update in Settings

## Fixed
- Opened `services.msc`
- Located **Windows Update**
- Started the service manually

## Confirmed
- Retested **Windows Update**
- Verified that the system could check for updates normally again after the service was restarted

## Real-World Relevance
This is a common IT support and desktop support issue.  
If the Windows Update service stops, users may be unable to receive security patches or system updates.  
This lab demonstrates practical troubleshooting of Windows services using built-in administrative tools.

## Tech Stack
- VirtualBox
- Windows 10
- `services.msc`
- Windows Update Settings

## Screenshots

### 1. Baseline (Windows Update working before issue)

![alt text](screenshots/Baseline.png)

### 2. Break (Windows Update service stopped + update issue)

![alt text](screenshots/Break.png)

### 3. Evaluate (Windows Update service stopped in services.msc)

![alt text](screenshots/Evaluate.png)

### 4. Fixed (service restarted + Windows Update working again)

![alt text](screenshots/Fixed.png)

## Lab Note
**Lab 7: Windows Service Failure (Windows Update Service Stopped)**

- **Scenario:** User reported that Windows Update was not working and updates could not be checked.  
- **Identified:** The Windows Update service was stopped.  
- **Evaluated:** `services.msc` showed the Windows Update service was not running.  
- **Fixed:** Started the Windows Update service.  
- **Confirmed:** Windows Update functioned normally again after the service was restarted and the update check was retested.  
- **Real-world relevance:** Common desktop support issue. Demonstrates practical Windows service troubleshooting using built-in Windows tools.