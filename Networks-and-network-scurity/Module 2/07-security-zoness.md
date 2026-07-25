# Network Segmentation & Security Zones

## What is Network Segmentation?

**Network segmentation** is the practice of dividing a network into smaller sections called **segments**.

Each segment has its own:
- Security rules
- Access permissions
- Traffic controls

### Benefits

- Improves security
- Limits unauthorized access
- Prevents attacks from spreading
- Makes network management easier

---

# Security Zones

A **security zone** is a segment of a network with specific security controls and access permissions.

Security zones separate trusted and untrusted parts of a network to protect sensitive resources.

---

# Example of Network Segmentation

### Hotel Wi-Fi

- **Guest Network**
  - Public Wi-Fi
  - Internet access only
  - Separate from internal systems

- **Staff Network**
  - Secure and encrypted
  - Access to hotel systems
  - Protected from guest devices

---

### Organization Subnets

Organizations often divide departments into separate **subnets**.

Example:

- Faculty subnet
- Student subnet

If one subnet becomes infected, administrators can isolate it without affecting the rest of the network.

---

# Types of Security Zones

## 1. Uncontrolled Zone

The **uncontrolled zone** is any network outside the organization's control.

### Examples

- Internet
- Public networks
- External users

---

## 2. Controlled Zone

The **controlled zone** contains the organization's protected internal networks.

It includes multiple security layers to protect valuable resources.

---

# Demilitarized Zone (DMZ)

## Definition

A **Demilitarized Zone (DMZ)** is a network segment that contains **public-facing services** while remaining separated from the internal network.

### Common Services

- Web servers
- DNS servers
- Email servers
- File servers
- Proxy servers

### Purpose

- Allows public access to selected services
- Protects the internal network from direct Internet exposure
- Acts as the network perimeter

---

# Internal Network

The **internal network** contains private organizational resources.

### Examples

- Employee computers
- Internal applications
- Databases
- Business systems
- Private servers

Only authorized users are allowed access.

---

# Restricted Zone

## Definition

The **restricted zone** contains the organization's most sensitive information.

### Examples

- Financial records
- Confidential business data
- Customer information
- Critical systems

Only users with specific privileges can access this zone.

---

# Firewall Placement

A typical secure network places firewalls between security zones.

```text
Internet
    │
Firewall
    │
DMZ
    │
Firewall
    │
Internal Network
    │
Firewall
    │
Restricted Zone
```

### Purpose

- Blocks unauthorized access
- Prevents attacks from spreading
- Provides multiple layers of defense

---

# Security Zones Summary

| Security Zone | Purpose | Examples |
|--------------|---------|----------|
| **Uncontrolled Zone** | Outside the organization's control | Internet, public networks |
| **DMZ** | Hosts public-facing services | Web, DNS, email, proxy, file servers |
| **Internal Network** | Stores organizational resources | Employee devices, databases, applications |
| **Restricted Zone** | Protects highly confidential data | Financial systems, sensitive databases |

---

# Benefits of Network Segmentation

- Limits lateral movement by attackers
- Isolates infected systems
- Protects sensitive information
- Improves access control
- Simplifies network management
- Strengthens overall security

---

# Importance for Security Analysts

Security analysts use network segmentation to:

- Separate critical systems from public services
- Reduce the impact of cyberattacks
- Enforce least-privilege access
- Improve incident containment
- Protect sensitive organizational data

---

# Key Takeaways

- **Network segmentation** divides a network into smaller segments with separate security rules and access permissions.
- **Security zones** help isolate trusted and untrusted parts of a network to improve security.
- The **uncontrolled zone** includes external networks such as the Internet.
- The **DMZ (Demilitarized Zone)** hosts public-facing services while shielding the internal network from direct exposure.
- The **internal network** contains private organizational resources, while the **restricted zone** stores the most sensitive systems and data.
- **Firewalls** placed between security zones create multiple layers of defense and help prevent attacks from spreading throughout the network.