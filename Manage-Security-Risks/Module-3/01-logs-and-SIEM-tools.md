# Logs and SIEM

## What is a Log?

A **log** is a record of events that occur within an organization's systems, applications, and networks.

Security analysts review logs to:

- Detect security incidents
- Identify threats and vulnerabilities
- Investigate suspicious activity
- Support incident response
- Monitor system health

---

# Common Log Sources

## 1. Firewall Logs

### Definition

A **firewall log** records network traffic that passes through a firewall.

### Includes

- Incoming internet connections
- Outgoing internet requests
- Allowed traffic
- Blocked traffic
- Suspicious connection attempts

### Example

A firewall blocks repeated login attempts from an unknown IP address and records the event.

---

## 2. Network Logs

### Definition

A **network log** records activity across the organization's network.

### Includes

- Devices joining the network
- Devices leaving the network
- Device-to-device communication
- Network connections
- Service access

### Example

A new unauthorized laptop connects to the corporate Wi-Fi.

---

## 3. Server Logs

### Definition

A **server log** records events related to servers and the services they provide.

### Includes

- User logins
- Login failures
- Username requests
- Password requests
- Website access
- Email activity
- File sharing events

### Example

Multiple failed login attempts are detected on a web server.

---

# Why Logs Are Important

Logs help security teams:

- Detect cyber attacks
- Investigate incidents
- Identify vulnerabilities
- Monitor user activity
- Support forensic investigations
- Meet compliance requirements

---

# SIEM (Security Information and Event Management)

## Definition

A **Security Information and Event Management (SIEM)** tool is a security application that **collects, centralizes, analyzes, and monitors log data** from multiple sources to detect security threats.

---

# What SIEM Does

A SIEM system:

- Collects logs from multiple devices
- Stores logs in a centralized location
- Analyzes events in real time
- Correlates related events
- Detects suspicious activity
- Generates security alerts
- Supports incident investigations

---

# Benefits of SIEM

- Centralized log management
- Real-time monitoring
- Faster threat detection
- Automated alerts
- Improved incident response
- Reduced manual log analysis
- Increased operational efficiency

---

# Why SIEM Configuration Matters

Every organization has unique security requirements.

SIEM tools must be:

- Configured correctly
- Customized for the environment
- Updated as new threats emerge
- Tuned to reduce false positives

Proper configuration helps ensure important threats are detected quickly.

---

# Log Sources Used by SIEM

SIEM tools commonly collect logs from:

- Firewalls
- Servers
- Network devices
- Endpoints
- Applications
- Operating systems
- Authentication systems
- Security tools (IDS/IPS, Antivirus)

---

# Security Analyst Responsibilities

Security analysts use logs and SIEM tools to:

- Monitor security events
- Review alerts
- Investigate suspicious activity
- Detect threats
- Respond to incidents
- Recommend security improvements

---

# Key Takeaways

- A **log** is a record of events occurring within systems and networks.
- The three common log sources are:
  - **Firewall Logs** – Record allowed and blocked network traffic.
  - **Network Logs** – Record network devices and communications.
  - **Server Logs** – Record server and service-related activities such as logins and file access.
- **SIEM (Security Information and Event Management)** centralizes, analyzes, and monitors log data from multiple sources.
- SIEM provides **real-time visibility, automated alerts, event correlation, and centralized log storage**, helping security analysts detect and respond to threats more efficiently.
- SIEM tools require continuous **configuration and customization** to adapt to new threats and an organization's evolving security needs.