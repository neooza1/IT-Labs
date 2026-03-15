# Lab 8: Disk Space Full (System Slow)

## Scenario
User reported: **"My computer is slow and storage is almost full."**  
This is a realistic desktop support issue where a large file consumes disk space, reducing available storage and affecting system performance.

## Identified
A large temporary file was consuming significant space on the **C:** drive.

## Evaluated (Systems Level)
- Opened **This PC** to check available disk space
- Confirmed that free space on the **C:** drive had dropped significantly
- Located the large file (`bigfile.tmp`) in the root of the **C:** drive

## Fixed
- Deleted the large temporary file from the **C:** drive
- Refreshed disk usage in **This PC**

## Confirmed
- Verified that free space on the **C:** drive increased again after the file was removed

## Real-World Relevance
This is a common IT support and desktop support issue.  
Large temporary files, downloads, or cached data can consume storage and cause systems to slow down.  
This lab demonstrates practical disk space troubleshooting and safe cleanup in Windows.

## Tech Stack
- VirtualBox
- Windows 10
- Command Prompt
- File Explorer
- This PC

## Screenshots
Screenshots were captured during the lab and saved locally for documentation.  
They will be added in a future repository cleanup pass.



## Lab Note
**Lab 8: Disk Space Full (System Slow)**

- **Scenario:** User reported that the computer was running slowly and storage space was critically low.  
- **Identified:** A large temporary file was consuming significant disk space on the C: drive.  
- **Evaluated:** Checked disk usage in This PC and located the large file in the root of the C: drive.  
- **Fixed:** Deleted the large temporary file to free up disk space.  
- **Confirmed:** Free space on the C: drive increased after removing the file.  
- **Real-world relevance:** Common desktop support issue. Demonstrates practical disk space troubleshooting and cleanup in Windows.
