# Sentinel-Lab-1
**Azure Sentinel Lab 1** 

This lab exercise involved setting up Azure resources (e.g. Resource Group & VM) and deploying Microsoft Defender for Cloud and Azure Sentinel as well as setting up detection rules via Log Analytics to detect a potential malicious action on a system. 

**At a high level view, here are the activities done in this lab:**
- Configured and deployed Azure Resources - Log Analytics Workspace, Virtual Machines, and Azure Sentinel
- Enabled Microsoft Defender for Cloud
- Implemented Network and Virtual Machine Security Best Practices
    - Just in Time connections to VM to prevent unauthorised access
- Utilised Data Connectors to bring data into Sentinel for Analysis
- Examined Windows Security Event logs
- Configured Windows Security Policies to log security events
- Utilised KQL to query Logs in Azure Sentinel
- Wrote custom rules to detect Microsoft Security Events in Log Analytics
- Referenced MITRE ATT&CK to better understand and mitigate common tactics, techniques used in attacks

Please refer to attached documentation for step-by-step actions taken, as well as all KQL queries used for setting up log analytics rules.

## Network Design and Topology
![Untitled](https://github.com/pattytechuk/Sentinel1/assets/167561785/65fc9cc7-86de-4479-b609-bc9511db89f1)
(Source: CyberWox)


## VM Security 
Here we set up Just in Time rules to prevent unauthorised access to the VM. RDP is allowed for a pre-set amount of time but only from specific IPs; anyone who does not meet this criteria is denied access as a result of this rule. 
![JIT](https://github.com/pattytechuk/Sentinel1/assets/167561785/3d6dbadd-3b97-42dd-8d07-87afffd153d6)


## Utilised Data Connectors to bring in data into Sentinel
Here I set up data connector 'Windows Security Events via AMA' to collect data from Windows VM.
![data connectors1](https://github.com/pattytechuk/Sentinel1/assets/167561785/cea10400-1094-4bc9-8721-d955b8224838)
![data connectors2](https://github.com/pattytechuk/Sentinel1/assets/167561785/93974495-b999-4c65-8957-c8510641ec2d)
![data connectors3](https://github.com/pattytechuk/Sentinel1/assets/167561785/7b66c32a-8adf-4795-84e3-dc8342282307)


## Examined Windows Security Event Logs


## Configured Windows Security Policy to log security event


## Utilised KQL to query Logs in Sentinel


## Wrote custom rules to detect security event in Sentinel Log Analytics


## Referenced MITRE ATT&CK to better understand attack and find mitigations
