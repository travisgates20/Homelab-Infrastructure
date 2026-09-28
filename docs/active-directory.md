# Active Directory Infrastructure

## Overview

The homelab includes a Windows Active Directory environment designed to provide hands-on experience with centralized identity management, authentication, policy enforcement, and Windows enterprise administration.

Active Directory Domain Services (AD DS) provides the foundation for managing Windows users, computers, and security policies within the lab.

## Environment

The Active Directory environment currently provides:

- Centralized user authentication
- Computer domain membership
- DNS services
- Group Policy management
- Centralized security configuration
- Administrative access control

Specific domain names, usernames, hostnames, and other operational details are intentionally excluded from public documentation.

## Organizational Structure

The directory is organized to support separation of systems and administrative responsibilities.

The structure is designed to allow Group Policy to be applied based on system or user role rather than configuring individual machines independently.

As the environment expands, the organizational structure will continue to evolve to support additional servers, clients, administrative accounts, and services.

## Domain-Joined Systems

Windows systems within the lab are joined to the Active Directory domain.

Domain membership allows systems to receive centralized:

- Authentication
- Group Policy
- Security configuration
- Account policies
- Audit policies

This provides a more realistic enterprise administration environment than managing each Windows system independently.

## Group Policy

Group Policy is used to centrally configure and enforce Windows settings across domain-joined systems.

Current areas of configuration include:

- Account policies
- Authentication controls
- Windows security settings
- Audit policies
- Microsoft Defender
- Windows Firewall
- User and computer restrictions

Security-focused Group Policy configuration is documented separately in the security-hardening documentation.

## DNS

DNS services support Active Directory and allow domain resources to locate required services within the environment.

DNS configuration is maintained as part of the Windows Server infrastructure.

## Administrative Model

Administrative access is separated from normal system use where practical.

The environment is being developed around principles including:

- Least privilege
- Centralized administration
- Role-based access
- Separation of administrative and standard user activity
- Consistent policy enforcement

## Security

Active Directory security is being developed incrementally as additional controls are implemented.

Areas of focus include:

- Password and account policies
- Authentication security
- Privileged account management
- Audit logging
- Group Policy security baselines
- STIG-aligned configuration
- Reduction of unnecessary privileges

## Future Development

Planned improvements include:

- Additional organizational unit design
- Expanded role-based security groups
- Improved administrative account separation
- Additional auditing and logging
- Expanded security baselines
- Integration with centralized monitoring
- Automated configuration where appropriate

Changes will be documented as they are implemented.
