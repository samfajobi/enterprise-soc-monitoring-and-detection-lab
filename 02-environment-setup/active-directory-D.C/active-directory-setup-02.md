# Windows 10 Domain Join Guide (Enterprise SOC Lab)

## Overview
This document provides a step-by-step procedure for **joining a Windows 10 endpoint to an Active Directory domain**.

Domain-joining a workstation allows:
- Centralized authentication
- Group Policy enforcement
- Realistic enterprise identity telemetry
- High-value security events for SOC monitoring and SIEM ingestion

---

## Lab Context

- **Domain Controller:** Windows Server (AD DS + DNS)
- **Client OS:** Windows 10
- **Network:** LAN behind pfSense
- **IP Assignment:** DHCP (client), Static (DC)
- **DNS:** Active Directory DNS on DC

---



