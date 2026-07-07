# Entry-Level Security Analyst Toolkit

## Logs

### What is a Log?
A **log** is a record of events that occur within an organization's systems.

### Examples
- Employee logins
- Access to web applications
- Network activity
- System events
- Security events

### Importance
- Detect vulnerabilities
- Identify security breaches
- Monitor system activity
- Support incident investigations

---

# Security Information and Event Management (SIEM)

## Definition
A **SIEM (Security Information and Event Management)** tool is an application that collects, analyzes, and monitors log data to identify security threats in real time.

## Why SIEM is Needed
Without SIEM:
- Analysts may spend hours or days reviewing logs manually.

With SIEM:
- Collects logs automatically
- Filters unnecessary data
- Detects threats in real time
- Generates alerts for suspicious activity
- Speeds up incident response

---

## SIEM Features
- Real-time monitoring
- Log collection from multiple sources
- Data analysis and filtering
- Security dashboards
- Threat detection
- Incident investigation
- Search capabilities

---

## SIEM Dashboards
SIEM tools organize information using dashboards that:
- Categorize security events
- Display alerts
- Allow analysts to search and filter logs
- Simplify investigation

---

## SIEM Hosting Options

### On-Premise
- Installed on company servers
- Greater control
- Requires maintenance and expertise

### Cloud
- Hosted by cloud providers
- Easier deployment
- Easier maintenance
- Faster updates
- Good for less experienced security teams

---

# Common SIEM Tools

## Splunk Enterprise
- Self-hosted SIEM platform
- Collects and stores logs
- Searches and analyzes log data
- Supports incident investigations

### Advantages
- Powerful search capabilities
- Flexible data analysis
- Widely used in enterprises

---

## Google Chronicle

- Cloud-native SIEM
- Stores massive amounts of security data
- Optimized for fast searching
- Frequently updated through the cloud

### Cloud-Native
Cloud-native means:
- Faster feature updates
- Easier scalability
- Lower maintenance

---

# How Security Analysts Use SIEM

Security analysts use SIEM tools to:
- Analyze security events
- Identify attack patterns
- Investigate incidents
- Hunt for threats proactively
- Reduce organizational risk

---

# Network Protocol Analyzer (Packet Sniffer)

## Definition
A **Network Protocol Analyzer**, also called a **Packet Sniffer**, captures and analyzes network traffic.

It records every packet traveling across a network.

---

## Uses
- Monitor network traffic
- Detect suspicious communications
- Troubleshoot network problems
- Analyze attacks
- Investigate incidents

---

## Common Packet Sniffers
- **Wireshark**
- **tcpdump**

---

# Playbooks

## Definition
A **Playbook** is a documented guide that outlines step-by-step procedures for performing security tasks or responding to incidents.

---

## Purpose
- Standardize security processes
- Ensure consistent incident response
- Meet compliance requirements
- Reduce human error

---

## Common Playbook Types
- Incident response
- Compliance reviews
- Access management
- Forensic investigations
- Disaster recovery

---

# Example Scenario

A small medical practice experiences a security breach.

A security analyst must:
- Investigate the incident
- Collect digital evidence
- Document findings
- Provide evidence to a cybersecurity insurance company

Playbooks ensure every investigation follows the correct procedures.

---

# Chain of Custody Playbook

## Definition
**Chain of Custody** is the process of documenting the possession and handling of evidence throughout an investigation.

---

## Purpose
- Maintain evidence integrity
- Prevent tampering
- Ensure evidence is legally admissible

---

## Information Recorded
- Who collected the evidence
- What evidence was collected
- When it was collected or transferred
- Where it was stored
- Why it was accessed
- Who currently possesses it

Every movement of evidence must be documented.

---

# Protecting and Preserving Evidence Playbook

## Definition
The process of safely handling fragile and volatile digital evidence to prevent alteration or loss.

---

## Best Practices
- Never investigate the original evidence.
- Create forensic copies.
- Perform analysis only on copies.
- Preserve original evidence securely.

---

# Order of Volatility

## Definition
The **Order of Volatility (OoV)** determines the sequence in which digital evidence should be collected.

Collect the most volatile data first because it may disappear if the system loses power.

---

## Examples

### Highly Volatile
- RAM contents
- Running processes
- Active network connections

### Less Volatile
- Hard drives
- SSD storage
- Archived files
- Backups

---

# Volatile vs Fragile Evidence

## Volatile Data
Data that disappears when power is lost.

Examples:
- RAM
- Active sessions
- Running applications

---

## Fragile Evidence
Evidence that can easily be modified, corrupted, or destroyed during an investigation.

Improper handling may make evidence unusable.

---

# Key Takeaways

- **Logs** record events occurring within systems.
- **SIEM tools** collect, analyze, and monitor logs in real time.
- SIEM tools reduce manual work through dashboards, filtering, and alerts.
- **Splunk Enterprise** is a self-hosted SIEM.
- **Google Chronicle** is a cloud-native SIEM.
- **Packet sniffers** capture and analyze network traffic.
- **Wireshark** and **tcpdump** are popular packet analyzers.
- **Playbooks** provide standardized security procedures.
- **Chain of Custody** tracks evidence possession.
- **Protecting and Preserving Evidence** ensures digital evidence remains valid.
- **Order of Volatility** prioritizes collecting data that may disappear first.

---

# Quick Revision

| Term | Definition |
|------|------------|
| Log | Record of events within a system |
| SIEM | Collects and analyzes log data for threat detection |
| Splunk Enterprise | Self-hosted SIEM platform |
| Google Chronicle | Cloud-native SIEM platform |
| Dashboard | Visual interface for analyzing security data |
| Packet Sniffer | Captures and analyzes network traffic |
| Wireshark | GUI-based packet analyzer |
| tcpdump | Command-line packet analyzer |
| Playbook | Step-by-step security procedure manual |
| Chain of Custody | Documentation of evidence handling |
| Protect & Preserve Evidence | Maintain evidence integrity using forensic copies |
| Order of Volatility | Priority order for collecting digital evidence |
| Volatile Data | Data lost when a system powers off |
| Fragile Evidence | Evidence that can easily be altered or destroyed |

---

# Resources for more information

- The Google Cybersecurity Action Team's [Threat Horizon Report](https://services.google.com/fh/files/blogs/gcat_threathorizons_full_sept2022.pdf) provides strategic intelligence for dealing with threats to cloud enterprise.

- The Cybersecurity & Infrastructure Security Agency (CISA) has a list of [Free Cybersecurity Services and Tools](https://www.cisa.gov/free-cybersecurity-services-and-tools). Review the list to learn more about open-source cybersecurity tools.

