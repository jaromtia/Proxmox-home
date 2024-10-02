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

## Tasks and Estimated Costs

| Task | Estimated Costs | Notes |
|------|-----------------|-------|
|Deploy WAF VM|$0|Using existing resources|
|Set up Reverse Proxy VM|$0|Nginx on Linux|
|Install Wazuh Server|$0|Self-hosted|
|Create internal network bridges|$0|Proxmox configuration|
|Configure hacking lab (Kali, Metasploitable, vulnerable Windows 10)|$0|VM setup|
|**TOTAL**|**$0**|All using existing hardware and open-source software|

## Closing Checklist

- [ ] All Deliverables Checked and Tested for Quality Requirements
- [ ] Deliver Documentation for Architecture and Configuration (*If Required*)
- [ ] Get Customer/Management/Stakeholder Sign-Off
- [ ] Reassign Personnel, Dispose of Surplus Equipment/Materials, and Release Facilities
- [ ] Document Project (*Problems, Lessons Learned, Etc.*)
- [ ] Report Final Project Status and Outcome to Customer/Management/Stakeholders
- [ ] Declare Project Completed

