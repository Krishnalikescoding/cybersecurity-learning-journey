# Network Hardening

## Overview

**Network hardening** focuses on securing network-related components and reducing vulnerabilities across a network.

While **OS hardening** focuses on device safety through measures such as patch updates, secure configurations, and account access policies, network hardening focuses on controls such as:

- Port filtering
- Network access privileges
- Network encryption
- Network segmentation
- Firewall configuration

Network hardening tasks can be performed:

- **Regularly:** Firewall rule maintenance, network log analysis, patch updates, and server backups.
- **Initially and updated as needed:** Port filtering, network access privileges, encryption, and other network configurations.

## Regular Network Hardening Tasks

### Firewall Rules Maintenance

Firewall rules should be regularly reviewed and maintained to ensure that network traffic is properly controlled.

### Network Log Analysis

**Log:** A record of events that occur within an organization's systems.

**Network Log Analysis:** The process of examining network logs to identify events of interest.

Security teams can use a **log analyzer** or **Security Information and Event Management (SIEM)** tool to perform network log analysis.

### Security Information and Event Management (SIEM)

**Security Information and Event Management (SIEM):** An application that collects and analyzes log data to monitor critical activities within an organization.

A SIEM:

- Collects security data from across a network
- Analyzes log data
- Presents security information on a centralized dashboard
- Helps analysts inspect and analyze security events
- Helps security teams respond to security events based on priority
- Identifies new or ongoing network vulnerabilities

The centralized dashboard is sometimes called a **single pane of glass** because it provides security information in one interface.

### SIEM Vulnerability Prioritization

SIEM reports can list vulnerabilities according to their priority.

Typical priority levels range from:

**High → Low**

High-priority vulnerabilities generally have a shorter deadline for mitigation than lower-priority vulnerabilities.

### Patch Updates

Network systems and devices should receive appropriate patch updates to address security vulnerabilities.

### Server Backups

Regular server backups are another network hardening practice that helps maintain system availability and recoverability.

## Network Hardening Configurations

Some network hardening tasks are performed once initially and then updated when necessary.

These include:

- Port filtering
- Network access privileges
- Network communication encryption
- Network segmentation
- Wireless protocol configuration

## Port Filtering

**Port Filtering:** A firewall function that blocks or allows specific port numbers to limit unwanted network communication.

A basic security principle is:

> Only the ports required for normal network operations should be allowed.

Unused ports should be disallowed whenever they are not required.

This helps reduce exposure to **port vulnerabilities** and limits unnecessary network communication.

## Wireless Protocol Security

Networks should use the most up-to-date wireless protocols available.

Older wireless protocols should be disabled when they are no longer required.

Keeping wireless protocols up to date helps reduce security risks associated with outdated protocols.

## Network Segmentation

**Network Segmentation:** The practice of dividing a network into isolated subnets or security zones.

Security analysts can use network segmentation to separate different departments or areas of an organization.

### Example

An organization could create separate subnets for:

- Marketing
- Finance

This helps ensure that problems affecting one subnet do not spread across the entire organization.

Network segmentation can also restrict access so that users only access the network areas required for their roles.

### Security Zones

Network segmentation can be used to separate different **security zones**.

A restricted zone containing highly classified or confidential information should be separated from the rest of the network.

This provides additional protection for sensitive data and limits access to authorized users.

## Network Encryption

All network communication should use up-to-date encryption standards.

**Encryption Standards:** Rules or methods used to conceal outgoing data and decrypt incoming data.

Encryption helps protect data while it is being transmitted across a network.

### Restricted Zones

Data within restricted network zones should use stronger encryption standards.

Higher encryption standards make protected data more difficult for unauthorized users to access.

## OS Hardening vs. Network Hardening

| OS Hardening | Network Hardening |
|---|---|
| Focuses on device and operating system security | Focuses on network-related security |
| Patch updates | Port filtering |
| Secure configuration | Network access privileges |
| Account access policies | Network segmentation |
| Password and access controls | Network encryption |
| Operating system security | Firewall and wireless protocol security |

## Key Takeaways

- **Network hardening** reduces vulnerabilities in network infrastructure and communication.
- Regular tasks include:
  - Firewall rule maintenance
  - Network log analysis
  - Patch updates
  - Server backups
- **SIEM** tools collect and analyze security logs and present information through a centralized dashboard.
- A SIEM dashboard may be referred to as a **single pane of glass**.
- **Port filtering** allows required ports and blocks unnecessary ones.
- Older wireless protocols should be disabled in favor of up-to-date protocols.
- **Network segmentation** separates networks into isolated subnets or security zones.
- Restricted zones containing confidential data should be separated from the rest of the network.
- Network communication should use current **encryption standards**.
- Network hardening combines multiple controls to reduce the overall attack surface and protect network resources.  