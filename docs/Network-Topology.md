# Network Topology

## Overview

The BlueSentinel SOC Lab operates within an isolated VMware virtual network designed to simulate an enterprise environment for security monitoring and attack simulation. All virtual machines communicate through a dedicated internal network, ensuring that testing activities remain isolated from the host operating system and external networks.

This architecture allows realistic security events and attack traffic to be generated without impacting production systems.

---

# Network Design

The lab consists of three primary virtual machines connected through a custom VMware virtual network (VMnet2).

| Virtual Machine | Role | IP Address |
|-----------------|------|------------|
| Wazuh Server (Ubuntu) | SIEM & Log Management | 192.168.50.10 |
| Kali Linux | Attacker Machine | 192.168.50.20 |
| Windows 10 | Monitored Endpoint | 192.168.50.30 |

---

# Network Diagram

```text
                    VMware Workstation
                  Internal Network (VMnet2)

        +---------------------------------------------+
        |                                             |
        |        192.168.50.0/24 Network              |
        |                                             |
        |   +-----------------------------+           |
        |   | Wazuh Server (Ubuntu)       |           |
        |   | 192.168.50.10               |           |
        |   | SIEM • Dashboard • Manager  |           |
        |   +-------------+---------------+           |
        |                 |                           |
        |                 |                           |
        |   +-------------+---------------+           |
        |   | Windows 10 Endpoint         |           |
        |   | 192.168.50.30               |           |
        |   | Wazuh Agent • Sysmon        |           |
        |   +-------------+---------------+           |
        |                 |                           |
        |                 |                           |
        |   +-------------+---------------+           |
        |   | Kali Linux                  |           |
        |   | 192.168.50.20               |           |
        |   | Attack Simulation           |           |
        |   +-----------------------------+           |
        |                                             |
        +---------------------------------------------+
```

---

# Communication Flow

The Windows endpoint continuously forwards Windows Event Logs and Sysmon telemetry to the Wazuh Server using the Wazuh Agent.

The Kali Linux machine is used to generate reconnaissance and attack activity against the Windows endpoint. These activities produce security events that are collected, analyzed, and visualized within the Wazuh Dashboard.

Traffic generated between the systems can also be captured and analyzed using Wireshark to establish network baselines and investigate security events.

---

# Network Components

### Wazuh Server

Responsibilities:

- Centralized log collection
- Security event analysis
- Alert generation
- Dashboard visualization
- Security monitoring

---

### Windows Endpoint

Responsibilities:

- Generate Windows Event Logs
- Generate Sysmon telemetry
- Execute normal user activities
- Execute simulated attack scenarios
- Send logs to Wazuh

---

### Kali Linux

Responsibilities:

- Network reconnaissance
- Attack simulation
- Vulnerability assessment
- Traffic generation for detection testing

---

# Design Considerations

The network was intentionally designed with the following objectives:

- Isolate the lab from external production networks.
- Maintain predictable communication using static IP addresses.
- Support realistic attack simulation.
- Enable centralized monitoring through Wazuh.
- Capture network traffic for forensic analysis.
- Provide a repeatable environment for future SOC exercises.

---

# Validation

The network topology was validated by:

- Successful ICMP communication between all virtual machines.
- Successful Wazuh Agent registration.
- Continuous log ingestion into the Wazuh Dashboard.
- Successful packet capture using Wireshark.
- Stable communication across the VMnet2 virtual network.

---

# Key Insights

- An isolated virtual network provides a safe environment for offensive and defensive security testing.
- Static IP addressing simplifies monitoring, log collection, and incident investigation.
- Separating attacker, endpoint, and monitoring infrastructure closely resembles enterprise SOC deployments.
- A clearly documented network topology improves troubleshooting and future scalability.