# Network Baseline

## Overview

The third phase of the BlueSentinel SOC Lab focused on establishing a network baseline by observing and analyzing normal system behavior before introducing any attack scenarios.

A baseline represents the expected state of network communications, endpoint activity, and system behavior under normal operating conditions. Establishing this baseline is essential for identifying anomalies, detecting malicious activity, and supporting effective incident investigations.

Network traffic was captured using Wireshark while performing routine user activities such as logging into the Windows endpoint, browsing the web, transferring files, and generating ICMP traffic.

---

# Objectives

- Capture normal network traffic.
- Identify commonly used protocols.
- Observe typical communication patterns.
- Analyze active endpoints.
- Examine network conversations.
- Establish a trusted baseline for future attack comparisons.

---

# Normal Activities Performed

The following activities were performed to generate baseline traffic:

- User logon
- ICMP Ping
- Web browsing
- File operations
- Windows background processes
- DNS and multicast name resolution
- Wazuh Agent communication

These activities represent expected behavior within the SOC environment.

---

# Traffic Capture

Traffic was captured using Wireshark from the Windows endpoint during normal system operation.

The resulting packet capture provides a reference point for future comparisons against malicious or abnormal network activity.

---

# Protocol Analysis

The captured traffic primarily consisted of the following protocols.

| Protocol | Purpose | Observation |
|----------|----------|-------------|
| TCP | Reliable communication | Primary protocol used throughout the capture |
| UDP | Service discovery and lightweight communication | Observed during normal Windows operations |
| ICMP | Connectivity testing | Generated during validation testing |
| ARP | Address Resolution | Normal local network communication |
| mDNS | Multicast Name Resolution | Windows service discovery traffic |
| IPv4 | Network communication | Dominant network protocol within the lab |

No abnormal or unexpected protocols were identified during the baseline capture.

---

# Port Analysis

Several commonly used ports were observed throughout the capture.

| Port | Service | Purpose |
|------|----------|----------|
| 1514 | Wazuh Agent | Log forwarding to Wazuh Server |
| 137 | NetBIOS | Windows name resolution |
| 5353 | mDNS | Multicast DNS |
| Dynamic High Ports | Windows Client Communication | Temporary outbound connections |

The observed ports aligned with expected Windows and Wazuh communication.

---

# Endpoint Analysis

Endpoint analysis identified the primary systems participating in network communication.

| Endpoint | Role |
|----------|------|
| Wazuh Server | Centralized monitoring platform |
| Windows Endpoint | Monitored system |
| Kali Linux | Security testing workstation |
| VMware Virtual Network | Internal communication infrastructure |

The observed endpoints matched the designed network topology.

---

# Conversation Analysis

Wireshark conversation statistics confirmed continuous communication between the monitored endpoint and the Wazuh Server.

Primary communication included:

- Windows Endpoint ↔ Wazuh Server
- Windows background services
- Network discovery traffic
- Wazuh Agent log forwarding

These conversations established the expected communication profile for the environment.

---

# Baseline Summary

The baseline analysis identified several characteristics of normal network behavior:

- Stable communication between all virtual machines.
- Continuous log forwarding from the Windows endpoint to the Wazuh Server.
- Expected Windows background network activity.
- Normal protocol distribution.
- No suspicious communication patterns.
- No unexpected endpoints.
- No abnormal ports.

This baseline serves as the reference point for all future attack simulations performed within the SOC lab.

---

# Validation

The baseline was validated through:

- Successful packet capture.
- Protocol Hierarchy analysis.
- Endpoint analysis.
- Conversation analysis.
- Port analysis.
- Continuous Wazuh monitoring.

These validation steps confirmed that the captured traffic accurately represents normal operating conditions.

---

# Deliverables

The following deliverables were successfully completed:

- Baseline packet capture (.pcapng)
- Protocol analysis
- Endpoint analysis
- Conversation analysis
- Port analysis
- Baseline documentation
- Supporting screenshots

---

# Outcome

At the conclusion of Phase 3, a comprehensive network baseline was established for the BlueSentinel SOC Lab.

This baseline provides a trusted reference against which future attack traffic, suspicious behavior, and security events can be compared. It also enables more accurate detection engineering, threat hunting, and incident investigation throughout the remaining phases of the project.

---

# Key Insights

- Understanding normal network behavior is essential before detecting malicious activity.
- Baselines significantly reduce false positives during security monitoring.
- Network traffic analysis provides valuable context during incident investigations.
- Combining endpoint telemetry with packet analysis improves overall detection capability.
- Establishing a baseline creates a measurable reference for evaluating future attack scenarios.