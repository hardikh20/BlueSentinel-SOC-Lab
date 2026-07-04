# IP-Address-Inventory

## Overview

The IP Address Inventory provides a structured record of all assets deployed within the BlueSentinel SOC Lab. Maintaining an accurate inventory is essential for effective security monitoring, incident response, and network management. Each system has a clearly defined role and a static IP address to ensure consistent communication throughout the lab environment.

---

# Asset Inventory

| Hostname | Operating System | IP Address | Role |
|----------|------------------|------------|------|
| Wazuh Server | Ubuntu Server | 192.168.50.10 | Centralized SIEM, Log Collection, Detection & Monitoring |
| Kali Linux | Kali Linux | 192.168.50.20 | Attack Simulation & Security Testing |
| Windows Endpoint | Windows 10 | 192.168.50.30 | Monitored Endpoint with Wazuh Agent & Sysmon |

---

# Network Information

| Network Parameter | Value |
|-------------------|-------|
| Virtual Network | VMnet2 |
| Network Type | Internal Virtual Network |
| Network Address | 192.168.50.0/24 |
| Addressing Method | Static IP Addressing |

---

# System Roles

## Wazuh Server (192.168.50.10)

Responsibilities:

- Centralized log collection
- Security event analysis
- Wazuh Manager
- Wazuh Indexer
- Wazuh Dashboard
- Alert generation

---

## Kali Linux (192.168.50.20)

Responsibilities:

- Attack simulation
- Network reconnaissance
- Vulnerability assessment
- Security testing
- Traffic generation

---

## Windows Endpoint (192.168.50.30)

Responsibilities:

- Execute normal user activity
- Generate Windows Event Logs
- Generate Sysmon telemetry
- Send logs through the Wazuh Agent
- Act as the monitored enterprise endpoint

---

# Communication Matrix

| Source | Destination | Purpose |
|--------|-------------|---------|
| Windows Endpoint | Wazuh Server | Send Windows and Sysmon logs |
| Kali Linux | Windows Endpoint | Generate attack and reconnaissance traffic |
| Windows Endpoint | Internet (when enabled) | Normal browsing and software updates |

---

# Validation

The inventory was verified through:

- Static IP configuration
- Successful ICMP connectivity between all virtual machines
- Wazuh Agent registration
- Successful log ingestion into the Wazuh Dashboard
- Continuous communication over the VMnet2 virtual network

---

# Key Insights

- Static IP addresses provide predictable communication paths for monitoring and incident response.
- Maintaining an accurate asset inventory simplifies troubleshooting, alert investigation, and future lab expansion.
- Clearly defined system roles improve visibility into the responsibilities of each component within the SOC architecture.# IP-Address-Inventory

