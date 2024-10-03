# Project Summary

**Project name:** Proxmox WAF, Reverse Proxy, and Security Infrastructure

**Project goal:** To design and deploy a network security architecture using WAF (ModSecurity), reverse proxy (Nginx), Wazuh server for security monitoring, and backend services, all hosted on a Proxmox environment.

## Objectives:

- Build a WAF using ModSecurity to filter incoming traffic
- Deploy a reverse proxy (Nginx) to route clean traffic to backend services
- Set up Wazuh for security monitoring and alerts
- Isolate backend services using an internal network bridge to secure the internal architecture
- Create a hacking lab with Kali Linux and vulnerable VMs for red team emulation (Metasploitable, Windows 10 with vulnerabilities)

## Constraints:

- Budget constrained by existing resources (32 GB RAM, 500 GB storage)
- Limited by hardware performance for running multiple virtual machines simultaneously
- Timeline to complete within the next two weeks
- Familiarity with Linux systems and network configuration

## Risks:

- Resource limitations affecting VM performance [**SIGNIFICANT RISK**]
- Incorrect firewall/network configuration exposing backend services [**SIGNIFICANT RISK**]
- Overload of storage due to logging in Wazuh and WAF [MODEST RISK]
- Delays in Wazuh deployment and configuration [MODEST RISK]

## Assumptions:

- Existing Proxmox server will handle all required VMs
- External internet access is available for updates and installations
- ModSecurity will effectively mitigate most common attack vectors
- Backend services will not require high bandwidth or high performance

## Project Scope

### In Scope:

- Deploy WAF (ModSecurity), reverse proxy (Nginx), Wazuh server, and backend services in Proxmox
- Create internal private network bridges for VM communication
- Configure a hacking lab with Kali Linux and vulnerable machines (e.g., Metasploitable, vulnerable Windows 10)

### Out of Scope:

- External penetration testing outside of the Proxmox environment
- Cloud-based or hybrid security services integration
- Handling production-level traffic (this is for a home lab setup)

## Deliverables:

- Fully configured WAF (ModSecurity) VM filtering traffic
- Reverse proxy VM forwarding traffic to backend services
- Wazuh server for real-time monitoring and alerting
- Isolated internal backend services connected via Proxmox network bridges
- Hacking lab environment for red team emulation

## Tasks and Resource Allocation

| Task | RAM Usage | Storage Usage | CPU Usage | Notes |
|------|-----------|---------------|-----------|-------|
| Deploy WAF VM (ModSecurity) | 2 GB | 20 GB | 1 core | Light traffic filtering load |
| Set up Reverse Proxy VM (Nginx) | 2 GB | 15 GB | 1 core | Low CPU demand unless traffic spikes |
| Install Wazuh Server | 4 GB | 30 GB | 2 cores | For security monitoring and alerting |
| Create internal network bridges | N/A | N/A | N/A | Network configuration in Proxmox |
| Configure hacking lab (Kali Linux) | 4 GB | 20 GB | 1 core | Penetration testing and hacking tools |
| Metasploitable VM | 1 GB | 10 GB | 1 core | Lightweight vulnerable system |
| Vulnerable Windows 10 VM | 8 GB | 40 GB | 2 cores | For red team attack emulation |
| **TOTAL** | **21 GB** | **135 GB** | **8 cores** | Within available resources |

## Closing Checklist

- [ ] All Deliverables Checked and Tested for Quality Requirements
- [ ] Deliver Documentation for Architecture and Configuration (*If Required*)
- [ ] Get Customer/Management/Stakeholder Sign-Off
- [ ] Reassign Personnel, Dispose of Surplus Equipment/Materials, and Release Facilities
- [ ] Document Project (*Problems, Lessons Learned, Etc.*)
- [ ] Report Final Project Status and Outcome to Customer/Management/Stakeholders
- [ ] Declare Project Completed

