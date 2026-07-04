# 🛡️ BlueSentinel SOC Lab – Enterprise Detection & Threat Monitoring Environment

## Overview

BlueSentinel SOC Lab is a self-hosted Security Operations Center (SOC) environment built to simulate enterprise security monitoring, endpoint visibility, and threat detection workflows.

The project focuses on building a complete SOC infrastructure from the ground up using industry-standard security tools. The lab is designed to replicate real-world blue team operations, enabling security analysts to monitor endpoints, collect telemetry, establish network baselines, investigate security events, and detect malicious activity in a controlled environment.

The project follows a phased implementation approach where each stage builds upon the previous one, gradually transforming a basic virtual environment into a fully operational SOC capable of detecting and investigating cyber threats.

---

## Project Objectives

- Build an enterprise-style SOC laboratory using virtual machines.
- Centralize Windows security logs using Wazuh.
- Monitor endpoint activity with Sysmon.
- Establish a normal network traffic baseline before introducing attacks.
- Simulate real-world attack scenarios for detection engineering.
- Develop hands-on experience with SOC operations, incident analysis, and threat monitoring.
- Document each implementation phase professionally.
- Showcase practical blue team skills through a production-style GitHub project.

---

## Current Project Status

| Phase | Status |
|-------|--------|
| Phase 1 – SOC Lab Deployment | ✅ Completed |
| Phase 2 – Monitoring Configuration | ✅ Completed |
| Phase 3 – Network Baseline | ✅ Completed |
| Phase 4 – Attack Simulation | ⏳ Planned |
| Phase 5 – Detection Engineering | ⏳ Planned |
| Phase 6 – Threat Hunting | ⏳ Planned |
| Phase 7 – Incident Investigation | ⏳ Planned |
| Phase 8 – SOC Reporting & Automation | ⏳ Planned |

---

## Lab Architecture

The SOC lab consists of three primary virtual machines connected through an isolated VMware virtual network.

| Component | Purpose |
|----------|----------|
| Windows 10 | Endpoint monitored by Wazuh and Sysmon |
| Kali Linux | Attack simulation and security testing workstation |
| Wazuh Server | Centralized log collection, detection, and monitoring platform |

The environment is intentionally isolated from production systems, allowing attacks and defensive monitoring to be performed safely.

---

## Technology Stack

### Virtualization

- VMware Workstation Pro

### Operating Systems

- Windows 10
- Kali Linux
- Ubuntu Server (Wazuh Server)

### Security Tools

- Wazuh
- Sysmon
- Wireshark

### Networking

- Internal Virtual Network
- Static IP Addressing
- ICMP
- TCP
- UDP
- DNS
- mDNS

### Documentation

- Visual Studio Code
- Markdown
- Git
- GitHub

---

## Repository Structure

```text
BlueSentinel-SOC-Lab/
│
├── docs/
│   ├── 01-SOC-Lab-Setup/
│   ├── 02-Monitoring-Configuration/
│   ├── 03-Network-Baseline/
│   ├── IP-Address-Inventory.md
│   ├── Network-Topology.md
│   └── Project-Architecture.md
│
├── screenshots/
├── reports/
├── network-captures/
├── diagrams/
├── configs/
├── resources/
│
├── README.md
├── LICENSE
└── .gitignore
```

---

## Skills Demonstrated

This project demonstrates practical experience with:

- Security Operations Center (SOC) fundamentals
- Windows Event Logging
- Endpoint Monitoring
- Sysmon Configuration
- Wazuh Deployment & Administration
- Network Traffic Analysis
- Wireshark Packet Analysis
- Network Baseline Development
- Virtual Lab Deployment
- Security Documentation
- Git & GitHub Version Control

---

## Project Roadmap

### Version 1.0
- ✅ Phase 1 – Build the SOC Lab
- ✅ Phase 2 – Configure Monitoring
- ✅ Phase 3 – Establish Network Baseline

### Version 2.0
- Attack Simulation
- Initial Detection Validation

### Version 3.0
- Detection Engineering
- Custom Wazuh Rules

### Version 4.0
- Threat Hunting
- IOC Analysis

### Version 5.0
- Incident Investigation
- SOC Reporting
- Detection Improvements

---

## Author

**Hardik Harchilkar**

Cybersecurity Student | Blue Team | SOC Analyst

LinkedIn:
https://www.linkedin.com/in/hardik-harchilkar-474433377

---

## License

This project is released under the MIT License.

---

> **Project Status:** Active Development 🚀

This repository is continuously updated as additional phases of the BlueSentinel SOC Lab are completed.