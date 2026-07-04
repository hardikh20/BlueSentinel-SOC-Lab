# Project Architecture

## Overview

The BlueSentinel SOC Lab is designed to simulate an enterprise Security Operations Center (SOC) environment for endpoint monitoring, centralized log collection, network traffic analysis, and threat detection.

The lab follows a modular architecture where each component has a dedicated responsibility. Windows acts as the monitored endpoint, Kali Linux is used to generate attack and reconnaissance activity, and the Wazuh Server functions as the centralized Security Information and Event Management (SIEM) platform.

---

## Architecture Components

### Windows 10 Endpoint

Role:
- Primary monitored endpoint
- Generates Windows Event Logs
- Generates Sysmon telemetry
- Sends security events to the Wazuh Server through the Wazuh Agent

---

### Kali Linux

Role:
- Security testing workstation
- Simulates attacker activity
- Performs reconnaissance and network scanning
- Generates attack traffic for detection and investigation

---

### Wazuh Server (Ubuntu)

Role:
- Centralized log collection
- Security event analysis
- Alert generation
- Endpoint monitoring
- Threat investigation dashboard

---

## Data Flow

```text
Windows Endpoint
        │
        │
   Sysmon Events
        │
        ▼
   Wazuh Agent
        │
        ▼
   Wazuh Manager
        │
        ▼
   Wazuh Indexer
        │
        ▼
 Wazuh Dashboard
```

---

## Communication Flow

```text
Kali Linux
      │
      │
      ▼
Windows Endpoint
      │
      │
      ▼
Wazuh Server
```

Normal user activity and attack simulations are performed against the Windows endpoint. Security events generated during these activities are forwarded to the Wazuh platform, where they are analyzed and visualized for investigation.

---

## Security Objectives

- Establish centralized security monitoring.
- Improve endpoint visibility using Sysmon.
- Collect and analyze Windows security events.
- Capture and analyze network traffic.
- Build a baseline of normal system behavior.
- Detect abnormal activity during simulated attacks.