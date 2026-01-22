# Splunk Enterprise SOC Monitoring Lab

This project demonstrates a **realistic enterprise Security Operations Center (SOC) monitoring environment** using **Splunk Enterprise**.  
It focuses on collecting, correlating, detecting, and investigating security events across **Windows endpoints, Active Directory, network firewalls (pfSense), and simulated attacks from Kali Linux**.

The lab is designed to showcase **SOC workflows**, **detection engineering**, and **incident response thinking**, rather than just tool installation.

---

## 🎯 Project Objectives

- Deploy Splunk Enterprise as a centralized SIEM
- Forward Windows Event Logs using Splunk Universal Forwarder
- Monitor Active Directory authentication and privilege activity
- Ingest and analyze pfSense firewall logs
- Simulate attacks using Kali Linux
- Create detections, dashboards, and alerts using SPL
- Apply SOC playbooks for investigation and response
- Map detections to MITRE ATT&CK

---

## 🏗️ Lab Architecture

### Components

| Component | Description |
|--------|------------|
| Splunk Enterprise | Central SIEM (Indexer + Search Head) |
| Windows Server | Active Directory Domain Controller |
| Windows Workstation | Domain-joined endpoint |
| Splunk Universal Forwarder | Log collection agent |
| pfSense Firewall | Network perimeter & firewall logs |
| Kali Linux | Attack simulation platform |

### Data Flow

Windows / Active Directory / pfSense
↓
Splunk Universal Forwarder
↓
Splunk Enterprise SIEM
↓
Searches • Alerts • Dashboards