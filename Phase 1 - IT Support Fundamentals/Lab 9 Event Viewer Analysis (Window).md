# Lab 9: Event Viewer Analysis (Windows Error Investigation)

**Scenario**  
User reports that a system component or background service is not functioning correctly.  
This is a common helpdesk and desktop support task where technicians use Windows diagnostic tools to investigate warnings, service failures, and system errors.

**Identified**  
- A **Service Control Manager** event was found in **Event Viewer** under **Windows Logs > System**.  
- This indicated a service-related warning/error requiring further investigation.

**Evaluated (Systems Level)**  
- Opened **Event Viewer** and reviewed the **System** log.  
- Located the relevant **Service Control Manager** event.  
- Inspected the event details, including:
  - **Source**
  - **Event ID**
  - **Level**
  - **General description**
- Used the event log information to understand the issue category and determine the likely next troubleshooting step.

**Fixed**  
- Performed diagnostic analysis using **Event Viewer** to identify the service-related issue.  
- Determined the next support action would involve checking:
  - service status,
  - startup type,
  - dependencies,
  - or restarting the affected service if required.

**Confirmed**  
- Successfully located and interpreted the relevant **Service Control Manager** event.  
- Confirmed the issue was correctly identified through log analysis.

**Real-World Relevance**  
Event Viewer is a core Windows troubleshooting tool used in helpdesk, desktop support, and IT operations roles to investigate service failures, application issues, and system warnings.  
This lab demonstrates evidence-based troubleshooting rather than guesswork.

**Tech Stack**  
- VirtualBox  
- Windows 10  
- Event Viewer (`eventvwr.msc`)  
- Windows Logs > System  
- Service Control Manager

**Screenshots**  

1. **Baseline – Event Viewer Open (System Log)**  

   <img width="1024" height="768" alt="Baseline" src="https://github.com/user-attachments/assets/491d15c9-ac2e-49ea-8bdb-b68b55027bb2" />


2. **Issue Detected – Service Control Manager Event Selected**  

   <img width="1024" height="768" alt="Break" src="https://github.com/user-attachments/assets/bc2566d5-354a-4726-8f07-17f1413e6e5e" />


4. **Evaluation – Event Details Reviewed (General Tab)**  

<img width="1024" height="768" alt="Evaluate" src="https://github.com/user-attachments/assets/0dd3aa1c-8b71-4bba-ac19-5d9d73b997f8" />


5. **Confirmed Diagnosis – Event Details Verified (Details Tab)**  

   <img width="1024" height="768" alt="Confirmed" src="https://github.com/user-attachments/assets/fa81c7c5-ed9b-4895-bff9-314fb11c1193" />


**Lab Note**  
Used Event Viewer to investigate a Service Control Manager event under Windows Logs > System.  
Reviewed the event source, event ID, level, and message details to identify the issue category and determine the likely next troubleshooting action.
