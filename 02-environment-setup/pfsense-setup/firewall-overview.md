# 🔥 Firewall Overview

## 📌 Introduction

A firewall is a network security device or software that monitors, filters, and controls incoming and outgoing traffic based on defined security rules.

It acts as a security boundary between trusted and untrusted networks and is one of the most critical security controls in modern enterprise environments.

---

## 🎯 Purpose of a Firewall

A firewall exists to:

* Enforce trust boundaries
* Control network access
* Reduce attack surface
* Prevent unauthorized access
* Provide visibility into traffic flows
* Log and monitor suspicious activity

At its core, a firewall answers:

Who can talk to who?  
On which port?  
Using which protocol?  
Under what conditions?

---

## 🌍 Understanding Network Zones

Firewalls operate between security zones. A zone represents a group of systems with similar trust levels.

### Common Enterprise Zones

## WAN (Untrusted Network)
* The Internet
* External partner networks
* Third-party connections

This zone is considered hostile and untrusted.

## LAN (Trusted User Network)
* Employee workstations
* Corporate laptops
* Internal endpoints

This zone contains regular users and internal devices.

## Server Network
* Domain Controllers
* File servers
* Database servers
* Application servers

This zone contains critical infrastructure.

## DMZ (Demilitarized Zone)
* Public web servers
* Email gateways
* Reverse proxies

Systems exposed to the internet are placed here to isolate them from internal networks.

## Guest Network
* Visitor WiFi
* Unmanaged devices

This network is isolated from internal systems.

---

## 🛡 Types of Firewalls

## Packet Filtering Firewall
* Filters traffic based on IP address, port, and protocol
* Stateless
* Basic level of control

## Stateful Firewall
* Tracks active connections
* Makes decisions based on connection state
* Most common traditional firewall type

## Next-Generation Firewall (NGFW)
* Deep packet inspection
* Application awareness
* Intrusion prevention (IDS/IPS)
* Threat intelligence integration

## Host-Based Firewall
* Installed directly on endpoints
* Controls inbound/outbound traffic per device

---

## 🔎 How Firewalls Work

1. Traffic enters an interface
2. Firewall checks rules top-down
3. If rule matches:
   * Allow or deny
4. If no rule matches:
   * Default deny (best practice)
5. Allowed traffic is logged and optionally inspected

Firewalls evaluate traffic on ingress (when it enters an interface).

---

## 🏢 How Firewalls Are Used in Organizations

Firewalls are deployed at multiple layers in enterprise environments.

## 1. Perimeter Firewall
* Sits between internal network and internet
* Controls north-south traffic
* Performs NAT
* Blocks unsolicited inbound traffic

## 2. Internal Segmentation Firewall
* Controls east-west traffic
* Separates user VLANs from server VLANs
* Restricts lateral movement

## 3. Data Center Firewall
* Protects critical infrastructure
* Controls access to databases and domain controllers

## 4. Cloud Firewall
* Protects cloud workloads
* Controls VPC/VNet traffic

---

## 🔐 Network Segmentation

Segmentation divides a network into smaller zones to limit the spread of attacks.

Example:

User VLAN → Can access Internet  
User VLAN → Can access Server VLAN only on required ports  
Guest VLAN → Cannot access internal networks  
Server VLAN → Limited outbound access  

Segmentation enforces least privilege and reduces blast radius during breaches.

---

## 📊 Firewall Logging and SOC Monitoring

Firewalls generate valuable logs including:

* Allowed and denied traffic
* Source and destination IPs
* Ports and protocols
* NAT translations
* Intrusion alerts (if IDS/IPS enabled)

SOC teams use firewall logs to:

* Detect port scans
* Identify brute force attempts
* Investigate lateral movement
* Monitor unusual outbound traffic
* Correlate alerts with endpoint logs

Firewalls are a primary log source in enterprise SIEM platforms.

---

## 🚨 Why Firewalls Matter in Security Operations

Without a firewall:
* Flat networks increase risk
* Malware spreads easily
* No visibility into traffic
* No enforcement of access control

With proper firewall architecture:
* Access is controlled
* Movement is restricted
* Suspicious activity is logged
* Incidents are easier to investigate

---

## 🧠 Key Security Principles Enforced by Firewalls

* Default Deny
* Least Privilege
* Segmentation
* Defense in Depth
* Visibility and Monitoring

---

## 📌 Summary

A firewall is not just a traffic blocker.

It is a policy enforcement engine that protects organizational assets, enforces trust boundaries, and provides visibility for security operations.

In enterprise environments, firewalls:

* Separate trusted and untrusted networks
* Control user and server access
* Protect critical infrastructure
* Enable SOC monitoring and threat detection

A properly configured firewall is foundational to any secure network architecture.
