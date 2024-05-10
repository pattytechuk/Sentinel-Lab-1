# Sentinel-Lab-1

## Azure Sentinel & Microsoft Defender Lab 

The objective of this project was to set up Azure resources (e.g. Resource Group & VM),  deploy Microsoft Defender for Cloud and deploy a SIEM (Azure Sentinel) to detect security events.
This lab project was adapted from [Cyberwox](https://cyberwoxacademy.com/azure-cloud-detection-lab-project/).

## Steps
Please refer to attached documentation for step-by-step actions taken, as well as all KQL queries used for setting up log analytics rules.

1. Sign up for Azure free account.
2. Deploy Microsoft Defender for Cloud - enable all plans.
3. Deploy Azure Sentinel workspace.
4. Create a new Azure Resource Group.
5. Create a new Azure Virtual Machine (VM).
6. Enable Just in Time access to VM to prevent unauthorised access and to provide access to only approved IPs for specified time.
7. Configure data connector 'Windows Security Events via AMA' in Sentinel to ingest and pull in data from VM's Windows Security Logs.
8. Log into VM.
9. Observe Security Logs in Windows Event Viewer.
10. Configure Scheduled Task in VM to open an application (i.e. Internet Explorer) to simulate a potentially malicious action; check in Security Logs for the event ID.
11. Create custom detection rule in Sentinel's Analytics to detect this event using KQL query.
12. Try a number of failed log in attempts on Windows VM to simulate another potentially malicious action.
13. Log into Windows VM and observe event ID in Event Viewer > Security Logs to capture event ID.
14. Go back to Azure Sentinel and configure second detection rule to detect this event using another KQL query.
15. Go to 'Incidents' in Azure Sentinel to observe incidents.
16. Reference MITRE ATT&CK framework to mitigate risk for these incidents.

## Network Design and Topology
<img src="https://github.com/pattytechuk/Sentinel-Lab-1/assets/167561785/1c631bdf-efd2-49dd-a621-85e73284f273" width="600" height="600" alt="MITRE ATT&CK">

(Source: CyberWox)

## Incidents in SIEM
![Untitled](https://github.com/pattytechuk/Sentinel-Lab-1/assets/167561785/3dd371f3-9fcf-4e52-a5d9-39685de2a883)

## Referencing MITRE ATT&CK framework 

**Risk of Failed Login Attempts:**

<img src="https://github.com/pattytechuk/Sentinel-Lab-1/assets/167561785/c3cd3351-ce7b-4ec8-8633-ad1d61f3ec37" width="600" height="300" alt="MITRE ATT&CK">

(Above: MITRE ATT&CK classification repeated failed log in attempts).

MITRE ATT&CK would classify this as a type of credential access technique - Brute Force (T1110) or Credential Stuffing (T1110).
**Risks:** Continuous failed login attempts can indicate an attempt to guess valid credentials through brute force or credential stuffing, leading to account compromise.
Denial of Service (DoS): Excessive failed login attempts can result in account lockouts, potentially causing a denial of service for legitimate users.
**Remediation Techniques (MITRE ATT&CK Mitigation):** Account lock out policies, rate limiting, 2FA, and monitoring/logging.

<img src="https://github.com/pattytechuk/Sentinel-Lab-1/assets/167561785/b8442358-6e0e-4639-bcc2-3b5b1f142793" width="600" height="300" alt="MITRE ATT&CK">

(Above: MITRE ATT&CK classification creation of schedule tasks).

**Risk of Creating Scheduled Tasks:**
MITRE ATT&CK would classify this as a persistent technique - Scheduled Task/Job (T1053).
**Risks:** Creating scheduled tasks without proper validation can result in executing unauthorized or malicious code. It's also associated with privilege escalation.
**Remediation Techniques (MITRE ATT&CK Mitigation):** Utilising Principle of Least Privilege for scheduled tasks; conducting regular audits and reviews of schedule dtasks to ensure they are legitimate; whitelisting to restrict execution of scheduled tasks to specifically approved scripts and commands.

## Resources
Please visit CyberWox's [site](https://cyberwoxacademy.com/azure-cloud-detection-lab-project/) for more information.

[MITRE ATT&CK framework](https://attack.mitre.org/).

