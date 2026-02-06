# SOC Architecture Overview

## Purpose
This document describes the architecture of the Enterprise SOC Monitoring environment used in this project. The architecture is designed to simulate a real-world enterprise network where logs from identity, endpoint, and network security controls are centrally collected, analyzed, and monitored by a Security Operations Center (SOC).

The primary objective of this architecture is to provide visibility, detection capability, and incident response readiness across multiple layers of the environment.

---

## High-Level Architecture Description
The SOC environment follows a centralized logging model where all security-relevant events are forwarded to a central SIEM platform (Splunk).

The architecture consists of:
- An **identity layer** (Active Directory)
- An **endpoint layer** (Windows 10 workstation)
- A **network security layer** (pfSense firewall)
- A **centralized monitoring layer** (Splunk SIEM)

All components are connected within a controlled lab network to replicate enterprise SOC monitoring workflows.

---

## Architecture Components

### Active Directory Domain Controller
The Active Directory Domain Controller serves as the central identity provider for the environment.

**Responsibilities:**
- User authentication and authorization
- Group and privilege management
- Centralized identity logging

**Security Telemetry Generated:**
- Authentication successes and failures
- Account lockouts
- Privilege and group membership changes

These logs are critical for detecting identity-based threats such as brute force attacks, password spraying, and unauthorized privilege escalation.

---

### Windows 10 Endpoint
The Windows 10 system represents a typical enterprise user workstation joined to the domain.

**Responsibilities:**
- User activity execution
- Endpoint-level security telemetry generation

**Security Telemetry Generated:**
- Process creation events
- Command-line execution
- User logon activity
- Persistence mechanisms

Endpoint telemetry provides visibility into suspicious execution behavior and post-compromise activity.

---

### pfSense Firewall
The pfSense firewall acts as the primary network security control and traffic inspection point.

**Responsibilities:**
- Network traffic filtering and logging
- Visibility into inbound and outbound connections
- Internal traffic monitoring

**Security Telemetry Generated:**
- Connection attempts
- Source and destination IPs
- Port and protocol usage
- Suspicious traffic patterns

Firewall logs support detection of port scanning, lateral movement, and anomalous network behavior.

---





---
