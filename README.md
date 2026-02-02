# PROJECT 1: USING WAZUH SIEM FOR REAL-TIME FILE INTEGRITY MONITORING (FIM)

 ## Project Overview

This project implements and validates a real-time File Integrity Monitoring (FIM) use case using Wazuh SIEM to monitor the Windows public directory:
`C:\Users\Public\`.
 Public directories are frequently abused by attackers for staging tools, dropping malware, and hiding payloads.
This project demonstrates how to detect unauthorized file activity in real time and generate actionable alerts for SOC operations.


## Real-World Problem 

**Attackers commonly abuse public or writable directories because they**:

- Allow broad user access
- Are easy locations to drop malicious files
- Are often under-monitored in many environments

**In a business environment, this creates a visibility gap where attackers can**:

- Stage malware
- Execute payloads
- Delete evidence before detection
  
Without real-time monitoring, these actions may go unnoticed

## What This Project Solves

**This implementation provides**:
- Immediate detection of unauthorized file creation and modification
- Faster incident response
- Reduced attacker dwell time on endpoints
- Increased visibility into endpoint abuse

##  Lab Architecture/ Tools

- Wazuh (SIEM Tool)
- Windows Server (Active Directory)
- Windows 10 Endpoint (Wazuh Agent Installed)
- Ubuntu server (Hosts Wazuh SIEM)
- Windows 11 Endpoint (Wazuh Agent)
  

## Configuration

The Windows public directory was added to the `ossec.conf` file to be Monitored Real time as per the Rule below: 

`<directories realtime="yes">C:\Users\Public</directories>`


I validated the setup by creating files in the monitored directory and confirming real time alerts in the Wazuh dashboard

## Results / Outcome

- File creation events detected instantly

- Alerts generated with filename, path, timestamp, and agent details

- Demonstrated end-to-end detection → alert → validation workflow

## Skills Demonstrated

- File Integrity Monitoring (FIM)
- Wazuh SIEM configuration
- Windows endpoint security monitoring
- SIEM alert validation and tuning
- SOC detection and investigation workflow
- Blue Team defensive monitoring

## Conclusion

This project demonstrates how real-time File Integrity Monitoring can be used to detect suspicious file activity in commonly abused Windows directories. By validating alerts end-to-end, the lab shows practical SOC skills and how proactive monitoring helps reduce attacker dwell time and improve incident response.






