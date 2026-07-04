# SOC Lab Setup

## Overview

The first phase of the BlueSentinel SOC Lab focused on designing and deploying a secure, isolated virtual environment capable of supporting enterprise-style Security Operations Center (SOC) activities.

The objective was to establish a stable infrastructure consisting of an attacker machine, a monitored endpoint, and a centralized Security Information and Event Management (SIEM) platform. This environment serves as the foundation for all subsequent monitoring, detection, investigation, and incident response activities.

---

# Objectives

- Build an isolated enterprise SOC laboratory.
- Deploy multiple virtual machines for attack simulation and security monitoring.
- Configure a dedicated internal virtual network.
- Assign static IP addresses for reliable communication.
- Verify connectivity between all systems.
- Prepare the infrastructure for centralized monitoring.

---

# Lab Environment

| Component | Technology |
|----------|------------|
| Virtualization Platform | VMware Workstation Pro |
| Attacker Machine | Kali Linux |
| Monitored Endpoint | Windows 10 |
| SIEM Platform | Ubuntu Server running Wazuh |

---

# Infrastructure Deployment

The SOC environment was deployed using three dedicated virtual machines connected through VMware's VMnet2 internal virtual network.

The deployment included:

- Windows 10 endpoint for telemetry generation.
- Kali Linux workstation for attack simulation.
- Ubuntu Server hosting the Wazuh SIEM platform.

Each virtual machine was configured with a static IP address to ensure predictable communication and simplify monitoring throughout the project.

---

# Network Configuration

The environment uses an isolated internal network to prevent interference with external systems while allowing unrestricted communication between the virtual machines.

Network Details:

- Virtual Network: VMnet2
- Network Type: Internal
- Addressing: Static IPv4

---

# Connectivity Validation

After configuring the environment, connectivity tests were performed between all virtual machines.

Validation included:

- ICMP communication between systems.
- Verification of static IP assignments.
- Successful communication across the internal virtual network.

These tests confirmed that the infrastructure was ready for centralized monitoring.

---

# Deliverables

The following deliverables were successfully completed during this phase:

- Enterprise SOC virtual environment.
- Three fully operational virtual machines.
- Internal virtual network.
- Static IP address allocation.
- Verified inter-machine connectivity.
- Foundation for centralized monitoring.

---

# Challenges Encountered

Several configuration challenges were addressed during the deployment process, including:

- Virtual network configuration.
- Static IP assignment.
- Inter-VM connectivity validation.
- Initial virtualization setup.

Resolving these issues provided a stable foundation for the remaining phases of the project.

---

# Outcome

At the end of Phase 1, the BlueSentinel SOC Lab infrastructure was fully operational and ready for monitoring configuration. The isolated environment successfully replicated the core components of an enterprise SOC architecture and established the foundation for endpoint monitoring, attack simulation, and security investigations.

---

# Key Insights

- A properly designed lab architecture is essential before implementing security monitoring.
- Static IP addressing improves operational consistency and simplifies incident investigation.
- Network isolation enables realistic attack simulation while protecting the host environment.
- Building a reliable infrastructure significantly reduces operational issues in later project phases.# SOC Lab Setup

