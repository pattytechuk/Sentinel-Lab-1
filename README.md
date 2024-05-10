# Sentinel-Lab-1
<img src="https://github.com/pattytechuk/Sentinel-Lab-1/assets/167561785/58ce9801-6a63-4bf7-a037-d562f72ece84" width="300" height="150" alt="Description of the image">

## Azure Sentinel & Microsoft Defender Lab 

The objective of this project was to set up Azure resources (e.g. Resource Group & VM),  deploy Microsoft Defender for Cloud and deploy a SIEM (Azure Sentinel) to detect security events.
This lab project was adapted from Cyberwox Academy.

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

<img src="https://github.com/pattytechuk/Sentinel1/assets/167561785/65fc9cc7-86de-4479-b609-bc9511db89f1" style="width:75%;" alt="Description of the image">

(Source: CyberWox)

## Incidents in SIEM
![Untitled](https://github.com/pattytechuk/Sentinel-Lab-1/assets/167561785/3dd371f3-9fcf-4e52-a5d9-39685de2a883)

## Usage

## Resources
