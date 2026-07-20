# BlueSentinel SOC Lab
### Enterprise Detection & Threat Monitoring Environment

![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux-blue)
![SIEM](https://img.shields.io/badge/SIEM-Wazuh-success)
![Monitoring](https://img.shields.io/badge/Monitoring-Sysmon-orange)
![Analysis](https://img.shields.io/badge/Analysis-Wireshark-yellow)
![Security](https://img.shields.io/badge/Security-Blue%20Team-red)

---

## Overview

BlueSentinel SOC Lab is an enterprise-style Security Operations Center (SOC) project developed to simulate a real-world blue team environment for security monitoring, network traffic analysis, threat investigation, and incident documentation.

The project demonstrates the complete SOC analyst workflow by integrating endpoint monitoring, centralized log collection, network packet analysis, and security event investigation within a virtual enterprise environment. The lab leverages **Wazuh SIEM**, **Sysmon**, **Wireshark**, **Kali Linux**, **Windows 10**, and **VMware Workstation** to simulate reconnaissance activities and analyze security telemetry from both network and endpoint perspectives.

---

# Project Objectives

- Design and deploy a virtual Security Operations Center (SOC) environment.
- Implement centralized security monitoring using Wazuh SIEM.
- Configure endpoint telemetry collection using Sysmon.
- Establish a baseline of normal network activity.
- Perform asset discovery and service enumeration.
- Simulate reconnaissance attacks using Nmap.
- Analyze network traffic using Wireshark.
- Investigate security events through Wazuh Threat Hunting.
- Produce professional SOC investigation documentation.

---

# Technology Stack

| Category | Technology |
|-----------|------------|
| Hypervisor | VMware Workstation |
| Operating Systems | Ubuntu Server, Windows 10, Kali Linux |
| SIEM Platform | Wazuh |
| Endpoint Monitoring | Sysmon |
| Network Analysis | Wireshark |
| Reconnaissance | Nmap |
| Documentation | GitHub Markdown |
| Version Control | Git |

---

# Lab Architecture

```
                        +----------------------+
                        |     Kali Linux       |
                        |    (Attacker VM)     |
                        +----------+-----------+
                                   |
                                   |
                         Reconnaissance Traffic
                                   |
                                   ▼
+--------------------------------------------------------------+
|                     Internal Virtual Network                 |
+--------------------------------------------------------------+
            |                                   |
            ▼                                   ▼
+----------------------+          +---------------------------+
|   Windows 10 VM      |          |      Wazuh Server         |
|                      |          |                           |
| • Sysmon             |--------->| Wazuh Manager            |
| • Wazuh Agent        |          | Wazuh Dashboard          |
|                      |          | Wazuh Indexer            |
+----------------------+          +---------------------------+

```

---

# Project Workflow

```
SOC Lab Deployment
        │
        ▼
Monitoring Configuration
        │
        ▼
Network Baseline Analysis
        │
        ▼
Asset Discovery
        │
        ▼
Reconnaissance Simulation
        │
        ▼
Packet Investigation
        │
        ▼
Alert Triage & Investigation
        │
        ▼
Incident Documentation
```

---

# Project Implementation

## Phase 1 — SOC Lab Deployment

Designed and deployed the virtual enterprise SOC environment by configuring VMware Workstation, Kali Linux, Windows 10, Ubuntu Server, and Wazuh SIEM.

---

## Phase 2 — Monitoring Configuration

Configured endpoint monitoring through Sysmon and integrated the Windows endpoint with Wazuh Agent to enable centralized log collection and security event monitoring.

---

## Phase 3 — Network Baseline

Established a baseline of legitimate network activity by capturing and analyzing normal communication patterns using Wireshark.

---

## Phase 4 — Asset Inventory

Performed network discovery using Nmap to identify live hosts, enumerate services, and document network assets within the SOC environment.

---

## Phase 5 — Reconnaissance Simulation

Simulated attacker reconnaissance by executing multiple Nmap scanning techniques to generate realistic network activity for subsequent investigation.

---

## Phase 6 — Packet Investigation

Performed detailed packet-level analysis using Wireshark to investigate TCP handshakes, SYN packets, connection attempts, protocol behavior, and network communication patterns.

---

## Phase 7 — Alert Triage & Investigation

Conducted security event analysis within Wazuh by reviewing alert metadata, endpoint telemetry, raw event logs, rule information, and investigation timelines to understand the alert investigation workflow.

---

## Phase 8 — Incident Documentation

Compiled the complete investigation into a professional SOC incident report documenting the investigation methodology, evidence, findings, analysis, and security recommendations.

---

# Skills Demonstrated

- Security Operations Center (SOC)
- Security Information and Event Management (SIEM)
- Endpoint Security Monitoring
- Windows Event Logging
- Network Traffic Analysis
- Packet Inspection
- Network Reconnaissance Analysis
- Asset Discovery
- Alert Triage
- Incident Investigation
- Security Event Correlation
- Network Baseline Analysis
- Technical Documentation

---

# Repository Structure

```
BlueSentinel-SOC-Lab
│
├── docs
│   ├── 01-SOC-Lab-Setup
│   ├── 02-Monitoring-Configuration
│   ├── 03-Network-Baseline
│   ├── 04-Asset-Inventory
│   ├── 05-Reconnaissance
│   ├── 06-Packet-Investigation
│   ├── 07-Alert-Triage
│   └── 08-Incident-Report
│
├── screenshots
│
├── reports
│
├── resources
│
└── README.md
```

---

# Learning Outcomes

This project provided practical experience in designing and operating a Security Operations Center (SOC) environment while developing skills in endpoint monitoring, security event analysis, network traffic investigation, asset discovery, packet analysis, alert triage, and professional incident documentation aligned with blue team methodologies.

---

# Future Enhancements

- Implement advanced custom detection rules.
- Integrate additional log sources.
- Simulate advanced adversary techniques mapped to the MITRE ATT&CK framework.
- Expand threat detection and incident response scenarios.
- Automate monitoring and reporting workflows.

---

# Author

**Hardik Harchilkar**

**Blue Team | SOC Analyst | Threat Detection | Security Monitoring**