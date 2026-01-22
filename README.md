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

Security events follow this pipeline:

1. **Data Sources**
   - Windows Endpoints
   - Active Directory Domain Controller
   - pfSense Firewall

2. **Log Collection**
   - Splunk Universal Forwarder collects and forwards logs

3. **SIEM Processing**
   - Splunk Enterprise indexes and processes events

4. **SOC Operations**
   - Correlation searches
   - Alert generation
   - Dashboards and investigations


---

## 🔍 Monitoring Scope

### Windows Endpoints
- Authentication successes and failures
- Account lockouts
- Privilege and group membership changes
- Process execution events

### Active Directory
- Domain logon activity
- Administrative account usage
- Privileged group modifications
- Suspicious authentication patterns

### pfSense Firewall
- Allowed and blocked traffic
- Port scanning indicators
- Suspicious inbound/outbound connections
- Network-based attack visibility

---

## ⚔️ Attack Simulation




