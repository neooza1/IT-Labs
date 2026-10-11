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

<img width="1024" height="768" alt="Baseline" src="https://github.com/user-attachments/assets/0932cb00-1b0f-4c06-bee9-49e20821cfe0" />


### 2. Break (Windows Update service stopped + update issue)

<img width="1024" height="768" alt="Break" src="https://github.com/user-attachments/assets/e57d3600-4858-4ca0-b63c-1c2014c2f9fd" />


### 3. Evaluate (Windows Update service stopped in services.msc)

<img width="1024" height="768" alt="Evaluate" src="https://github.com/user-attachments/assets/7794dd35-a4a0-4a44-8b16-2a4656ba92d0" />


### 4. Fixed (service restarted + Windows Update working again)

<img width="1024" height="768" alt="Fixed" src="https://github.com/user-attachments/assets/6084e66e-a0ea-47b1-b431-a173169e1f5f" />


## Lab Note
**Lab 7: Windows Service Failure (Windows Update Service Stopped)**

- **Scenario:** User reported that Windows Update was not working and updates could not be checked.  
- **Identified:** The Windows Update service was stopped.  
- **Evaluated:** `services.msc` showed the Windows Update service was not running.  
- **Fixed:** Started the Windows Update service.  
- **Confirmed:** Windows Update functioned normally again after the service was restarted and the update check was retested.  
- **Real-world relevance:** Common desktop support issue. Demonstrates practical Windows service troubleshooting using built-in Windows tools.
