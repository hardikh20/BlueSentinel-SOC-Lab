# Monitoring Configuration

## Overview

The second phase of the BlueSentinel SOC Lab focused on implementing centralized security monitoring by integrating the Windows endpoint with the Wazuh Security Information and Event Management (SIEM) platform.

The primary objective was to collect endpoint telemetry, monitor Windows security events, and provide centralized visibility into system activity. This phase established the monitoring foundation required for threat detection, incident investigation, and future attack simulations.

---

# Objectives

- Configure centralized security monitoring.
- Deploy the Wazuh Agent on the Windows endpoint.
- Install Sysmon to enhance endpoint telemetry.
- Collect Windows Event Logs.
- Verify successful log ingestion into the Wazuh Dashboard.
- Ensure the monitoring infrastructure was operational.

---

# Monitoring Architecture

The monitoring infrastructure consists of three primary components working together to collect and analyze endpoint telemetry.

| Component | Purpose |
|----------|----------|
| Windows 10 Endpoint | Generates security events and endpoint telemetry |
| Wazuh Agent | Collects and forwards logs to the Wazuh Server |
| Wazuh Server | Processes, stores, analyzes, and visualizes security events |

---

# Sysmon Deployment

Sysmon (System Monitor) was installed on the Windows endpoint to extend native Windows logging capabilities.

The deployment provides enhanced visibility into endpoint activities, including:

- Process creation
- Network connections
- File creation
- Registry modifications
- Driver loading
- Image loading
- Process termination

This additional telemetry significantly improves detection capabilities compared to standard Windows Event Logs.

---

# Wazuh Agent Configuration

The Wazuh Agent was deployed on the Windows endpoint and registered with the Wazuh Server.

Its primary responsibilities include:

- Collecting Windows Event Logs
- Forwarding Sysmon telemetry
- Maintaining continuous communication with the Wazuh Server
- Supporting centralized endpoint monitoring

---

# Log Collection Workflow

```text
Windows Endpoint
        │
        │
Windows Event Logs
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

The Wazuh platform processes incoming telemetry and presents security events through a centralized dashboard for monitoring and investigation.

---

# Validation

The monitoring configuration was verified through the following checks:

- Successful Wazuh Agent registration.
- Healthy agent status within the Wazuh Dashboard.
- Continuous Windows Event Log collection.
- Successful Sysmon event ingestion.
- Stable communication between the Windows endpoint and the Wazuh Server.

These validation steps confirmed that centralized monitoring was functioning as expected.

---

# Deliverables

The following deliverables were successfully completed:

- Wazuh Agent deployment.
- Sysmon installation.
- Centralized Windows Event Log collection.
- Endpoint telemetry integration.
- Healthy Wazuh Agent communication.
- Functional Wazuh Dashboard monitoring.

---

# Challenges Encountered

During deployment, several configuration challenges were identified and resolved, including:

- Wazuh Agent registration.
- Network communication verification.
- Sysmon configuration.
- Log forwarding validation.

Addressing these issues ensured reliable and continuous security monitoring.

---

# Outcome

At the conclusion of Phase 2, the Windows endpoint was fully integrated with the Wazuh SIEM platform. Security events and Sysmon telemetry were successfully collected, processed, and visualized, providing centralized visibility into endpoint activity.

This monitoring infrastructure established the foundation for future detection engineering, attack simulation, and incident investigation.

---

# Key Insights

- Centralized log collection enables efficient security monitoring and investigation.
- Sysmon significantly enhances endpoint visibility beyond default Windows logging.
- Continuous telemetry collection is essential for effective threat detection.
- Validating log flow before attack simulation ensures reliable detection results during later phases.