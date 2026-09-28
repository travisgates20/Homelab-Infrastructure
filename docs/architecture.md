# Homelab Architecture

## Overview

This homelab is an isolated environment designed for hands-on experience with enterprise infrastructure, systems administration, security, networking, and automation.

The environment is built around three physical systems running Proxmox VE. Virtual machines hosted within the environment provide Windows and Linux infrastructure while maintaining separation from the primary home network.

The lab is designed to evolve over time as additional infrastructure, security controls, automation, and containerized services are implemented.

## Architecture Goals

The environment is designed to:

- Provide an isolated platform for infrastructure experimentation
- Practice virtualization and systems administration
- Build and manage Windows Server infrastructure
- Administer Active Directory and Group Policy
- Implement and test security-hardening configurations
- Develop Linux administration skills
- Practice network design and troubleshooting
- Provide infrastructure for future Kubernetes deployments
- Introduce Infrastructure as Code and automation

## Physical Infrastructure

The compute layer consists of three physical HP systems configured as Proxmox VE hosts.

| Component | Role |
|---|---|
| Proxmox Host 1 | Virtualization host |
| Proxmox Host 2 | Virtualization host |
| Proxmox Host 3 | Virtualization host |
| Management Workstation | Administrative access to the lab |

The physical hosts provide compute resources for Windows Server, Windows client, Linux, and future container infrastructure.

## Virtualization

Proxmox VE provides the primary virtualization platform for the environment.

The virtualization layer allows the lab to support multiple isolated systems and services without requiring dedicated physical hardware for each workload.

Current and planned workloads include:

- Windows Server
- Windows client systems
- Linux servers
- Infrastructure services
- Kubernetes nodes
- Security and monitoring services

## Network Architecture

The homelab operates on a dedicated private network:

`192.168.100.0/24`

The lab network is separated from the primary home network to provide an isolated environment for infrastructure configuration, testing, and security experimentation.

Administrative access is performed from a dedicated management workstation connected to the lab network.

Individual host addresses and other operational details are intentionally excluded from public documentation.

### Current Topology

```text
                 Management Workstation
                          |
                          |
                    Lab Network
                  192.168.100.0/24
                          |
              +-----------+-----------+
              |           |           |
              v           v           v
          Proxmox      Proxmox      Proxmox
           Host 1       Host 2       Host 3
              |           |           |
              +-----------+-----------+
                          |
                  Virtual Workloads


```

## Windows Infrastructure

Windows Server infrastructure provides centralized identity, policy management, and supporting services within the lab.

Current areas of development include:

- Active Directory Domain Services
- DNS
- Domain-joined Windows clients
- Group Policy
- Centralized user and computer management
- Security policy enforcement
- Windows auditing and logging

  The Windows environment is intended to model common enterprises administration and security practices.

  ## Security

  Security is incorporated into the environment as part of the infrastructure design rather than treated as a separate component.

  Current areas of focus include:

  - Group Policy security configuration
  - Account and authentication policies
  - Windows auditing
  - security logging
  - Microsoft Defender configuration
  - Windows Firewall configuration
  - Principle of least privilege
  - STIG-aligned security hardening
 
  Security controls are implemented incrementally and documented as the lab develops.

  ## Planned Architecture

  Future phases of the homelab are expected to include:

  - Kubernetes cluster deployment
  - Infrastructure as Code with Terraform
  - Configuration automation
  - Centralized logging and monitoring
  - Expanded network segmentation
  - Linux infrastructure services
  - Containerized applications
  - Additional security monitoring and hardening
 
  These components will be documented as they are implemented rather than represented as existing infrastructure.

  ## Architecture Decisions

  Major architecture decisions will be documented throughout the project to capture both the implementation and the reasoning behind it.

  Areas that will be documented include:

  - Network isolation strategy
  - Virtualization architecture
  - Active Directory design
  - Group Policy organization
  - Security baseline decisions
  - Kubernetes architecture
  - Infrastructure autoamtion
  - Monitoring and logging strategy
 
  ## Documentation

  Additional technical documentation will be added as individual components of the environment are developed.
  










