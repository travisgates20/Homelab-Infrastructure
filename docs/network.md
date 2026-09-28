# Network Architecture

## Overview

The homelab uses a dedicated private network to provide an isolated environment for infrastructure administration, testing, and security experimentation.

The lab is intentionally separated from the primary home network to reduce the risk of configuration changes, testing, or experimental services affecting production household devices.

## Network Design

The current lab network uses the following private subnet:

`192.168.100.0/24`

The network provides connectivity between:

- Proxmox VE hosts
- Virtual machines
- Windows Server infrastructure
- Domain-joined clients
- Linux systems
- Dedicated management workstation

Individual host addresses are intentionally excluded from public documentation.

## Management Access

A dedicated management workstation is used to administer the homelab.

Administrative access includes:

- Proxmox VE web management
- Remote Desktop Protocol (RDP)
- Windows Server administration
- Active Directory management
- Group Policy management
- SSH access to Linux systems

Using a dedicated management system provides a consistent administrative entry point into the isolated environment.

## Network Topology

```text
                 Primary Network
                       |
                 [Isolation]
                       |
                Homelab Network
              192.168.100.0/24
                       |
        +--------------+--------------+
        |              |              |
        v              v              v
    Proxmox        Proxmox        Proxmox
     Host 1         Host 2         Host 3
        |              |              |
        +--------------+--------------+
                       |
                Virtual Systems
                       |
          +------------+------------+
          |                         |
          v                         v
   Windows Infrastructure      Linux Systems


          Management Workstation
                    |
                    +---- Administrative Access

```

## Design Considerations

### Isolation

The lab is separated from the primary network so infrastructure experiments and configuration changes can be performed without unnecessarily affecting other devices.

### Dedicated Management

Administrative access is performed from a dedicated workstation rather than relying on a general-purpose household systems.

### Private Addressing

RFC 1918 private addressing is used throughout the environment. Public documentation includes the lab subnet but excludes individual host addresses.

### Expandability

The network is designed to evolve as additional services are introduced.

Future network development may include:

- VLAN segmentation
- Dedicated management network
- Server and client VLANS
- Kubernetes networking
- Firewall segmentation
- Centralized monitoring
- Additional security controls

## Current Status

The isolated lab network is operational and provides management connectivity to the Proxmox infrastructure and hosted systems.

Additional segmentation and security controls will be documented as they are implemented
