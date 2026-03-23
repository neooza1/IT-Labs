# Lab 14: DNS Configuration and Name Resolution (Windows Server 2022)

## Scenario
User could ping the server by IP but not by hostname (server.lab.local). Common real-world issue where DNS name resolution fails.

## Identified
Missing or incorrect A record in DNS zone.

## Evaluated
- Checked DNS Manager on Domain Controller.
- Confirmed forward lookup zone (lab.local) existed.
- Ran nslookup and ping from Windows 10 client.

## Fixed
1. Created A record:
   - Name: server
   - IP: 192.168.10.10
   - Enabled PTR record
2. On client: `ipconfig /flushdns`

## Confirmed
- `ping server.lab.local` succeeded
- `nslookup server.lab.local` returned correct IP
- Connectivity worked using hostname

## Real-World Relevance
DNS is the backbone of Active Directory. Broken name resolution causes authentication failures, file share issues, and service problems in every company and government department.

## Tech Stack
- Windows Server 2022 (Domain Controller + DNS role)
- Windows 10 Pro client
- DNS Manager
- Command Prompt

## Screenshots
1. Baseline (failed nslookup)  
   ![Baseline](Lab14_Baseline.png)

2. A record created in DNS Manager  
   ![A Record](Lab14_ARecord.png)

3. Flush DNS + successful ping/nslookup  
   ![Fixed](Lab14_Fixed.png)

4. Confirm (hostname resolution working)  
   ![Confirm](Lab14_Confirm.png)