# SOC Detection & Incident Analysis Lab

## Overview
This project demonstrates the deployment and verification of a Security Information and Event Management (SIEM) platform within a virtualized lab environment. The goal of the lab is to build foundational Security Operations Center (SOC) skills, including SIEM deployment, monitoring, and preparation for endpoint log ingestion and threat detection.

The project is designed to support hands-on cybersecurity learning and to serve as a practical portfolio artifact for SOC and cybersecurity internship applications.

---

## Objectives
- Deploy a functional SIEM platform
- Establish centralized security monitoring
- Verify backend SIEM services and web dashboard access
- Prepare the environment for endpoint log ingestion and detection
- Document deployment decisions and validation steps

---

## Environment
- **Host Operating System:** Windows  
- **Virtualization Platform:** Oracle VirtualBox  
- **SIEM Platform:** Wazuh  
- **SIEM Operating System:** Ubuntu Server 22.04 LTS  

---

## Architecture
The lab consists of a centralized SIEM server running Wazuh on Ubuntu Server within a VirtualBox virtual machine. Networking is configured using a NAT-based design to ensure reliable outbound connectivity during deployment.

To allow secure access to the SIEM web interface from the host system, port forwarding is used to expose the Wazuh dashboard without directly bridging the virtual machine to the local network.

---

## Implementation Status
- [x] VirtualBox installed and configured
- [x] Ubuntu Server deployed for SIEM
- [x] Network connectivity verified
- [x] System packages updated
- [x] Wazuh SIEM installed (Manager, Indexer, Dashboard)
- [x] Wazuh services verified as running
- [x] Wazuh dashboard accessed via port forwarding
- [ ] Windows endpoint deployment
- [ ] Wazuh agent installation
- [ ] Log ingestion and alert generation
- [ ] Incident analysis and reporting

---

## Tools & Technologies
- Ubuntu Server 22.04 LTS  
- Wazuh SIEM  
- Oracle VirtualBox  
- Linux system administration tools  

---

## SIEM Verification

The following screenshots demonstrate successful deployment and verification of the Wazuh SIEM platform.

### Wazuh Manager Service Status
The screenshot below confirms that the Wazuh Manager service is active and running, indicating that the SIEM backend is operational.

![Wazuh Manager Running](screenshots/wazuh-manager-status.png)

### Wazuh Dashboard Interface
The screenshot below shows the Wazuh web dashboard, confirming successful access to the SIEM interface and readiness for endpoint monitoring.

![Wazuh Dashboard](screenshots/wazuh-dashboard.png)

---

## Design Decisions & Challenges
During initial setup, multiple network configurations were evaluated. To reduce complexity and ensure deployment stability, the design was simplified to a NAT-based architecture. Port forwarding was implemented to securely expose the Wazuh dashboard to the host system while maintaining isolation of the virtual machine.

This approach allowed focus to remain on SOC functionality rather than extended infrastructure troubleshooting.

---

## Next Steps
- Deploy a Windows endpoint for monitoring
- Install Sysmon for enhanced endpoint telemetry
- Install and configure the Wazuh agent
- Simulate attack activity and analyze detections
- Produce incident response documentation and reports

---

## Disclaimer
This project is conducted in a controlled lab environment for educational and defensive security purposes only. No unauthorized systems or networks are targeted.
