# File Integrity Monitoring (FIM) on Windows Server using Wazuh

## Overview
File Integrity Monitoring (FIM) is a security capability used to detect **unauthorized changes to critical files and directories**. Attackers often modify system files, configuration files, or sensitive directories to maintain persistence, escalate privileges, or evade detection.

This project demonstrates how to **configure and monitor File Integrity Monitoring on a Windows Server using Wazuh**, analyze alerts in the Wazuh dashboard, and perform SOC-style investigation and documentation.

---

## Objectives
- Configure File Integrity Monitoring on a Windows Server
- Detect file creation, modification, deletion, and permission changes
- Monitor and analyze FIM alerts in Wazuh
- Correlate Wazuh alerts with Windows Security Event Logs
- Map detected activities to the MITRE ATT&CK framework
- Practice real-world SOC alert triage

---

## Lab Architecture

- **Wazuh Manager:** Ubuntu Server
- **Wazuh Dashboard:** Web UI
- **Wazuh Agent:** Windows Server

```

[Windows Server + Wazuh Agent] → [Wazuh Manager] → [Wazuh Dashboard]

```

---

## Tools & Technologies
- Wazuh SIEM/XDR
- Windows Server
- Windows Security Event Logs
- PowerShell
- MITRE ATT&CK Framework

---

## Why File Integrity Monitoring Matters
File integrity monitoring helps detect:
- Unauthorized configuration changes
- Persistence mechanisms
- Tampering with system or application files
- Insider threats
- Malware attempting to hide or modify artifacts

FIM is commonly used in **enterprise SOCs, regulated environments, and compliance-driven organizations**.

---

## Monitored Directories (Example)
The following directories were selected due to their security relevance:

- `C:\Windows\System32`
- `C:\Program Files`
- `C:\SensitiveData` (custom test directory)

These locations often contain files targeted during post-exploitation and persistence activities.

---

## Step 1: Configure File Integrity Monitoring on Windows Server

On the Windows Server, edit the Wazuh agent configuration file:

```

C:\Program Files (x86)\ossec-agent\ossec.conf

````