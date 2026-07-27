# Subnetting

## What is Subnetting?

**Subnetting** is the process of dividing one large network into multiple smaller networks called **subnets**.

Each subnet functions as an independent network with its own devices, improving efficiency, organization, and security.

Think of a large network as a **city**, where each subnet is a different **neighborhood**.

---

# Why Subnetting is Used

Subnetting helps organizations:

- Improve network performance
- Reduce unnecessary network traffic
- Organize devices into logical groups
- Increase security through network isolation
- Create security zones
- Use IP addresses more efficiently

---

# What is a Subnet?

A **subnet (subnetwork)** is a smaller network created from a larger network.

Devices on the same subnet communicate directly without sending traffic through other subnets, making communication faster and more efficient.

---

# How Subnetting Works

Each device is assigned:

- An **IP address**
- A **Subnet Mask (Network Mask)**

The combination of these identifies which subnet the device belongs to.

Devices within the same subnet communicate locally, while communication between different subnets is handled by a **router**.

---

# Classless Inter-Domain Routing (CIDR)

## Definition

**Classless Inter-Domain Routing (CIDR)** is the modern method of assigning subnet masks to IP addresses.

It replaces the older **Classful Addressing** system.

### CIDR Format

```text
IP Address / Prefix Length
```

Example:

```text
198.51.100.0/24
```

- **198.51.100.0** → Network address
- **/24** → Network prefix (Subnet Mask)

A **/24** network includes addresses from:

```text
198.51.100.0
to
198.51.100.255
```

---

# Classful vs CIDR Addressing

| Classful Addressing | CIDR Addressing |
|---------------------|-----------------|
| Fixed network classes (A-E) | Flexible subnet sizes |
| Less efficient | More efficient |
| Limited IP allocation | Better use of IPv4 addresses |
| Older method | Modern standard |

---

# Security Benefits of Subnetting

Subnetting helps organizations:

- Isolate departments or business units
- Reduce the spread of cyberattacks
- Improve access control
- Create security zones
- Increase network performance
- Make network management easier

---

# Example

A university can divide its network into separate subnets:

- Student Network
- Faculty Network
- Administration Network
- Research Network

If malware infects the **Student Network**, administrators can isolate that subnet to help prevent the attack from spreading to the others.

---

# Subnetting and Security Zones

Subnetting is commonly used to build security zones such as:

- **DMZ**
- **Internal Network**
- **Restricted Zone**

Each subnet can have its own:

- Firewall rules
- Access permissions
- Security policies

---

# Subnetting Summary

| Term | Description |
|------|-------------|
| **Subnet** | A smaller network created from a larger network |
| **Subnetting** | Dividing a network into multiple subnets |
| **Subnet Mask** | Identifies the network and host portions of an IP address |
| **CIDR** | Modern method of subnetting using prefix notation (e.g., `/24`) |

---

# Importance for Security Analysts

Security analysts use subnetting to:

- Improve network organization
- Strengthen access control
- Isolate critical systems
- Reduce attack surfaces
- Contain security incidents
- Improve network performance

---

# Key Takeaways

- **Subnetting** divides a large network into smaller **subnets**, improving efficiency, organization, and security.
- A **subnet** is an independent section of a network identified by an **IP address** and **subnet mask**.
- **CIDR (Classless Inter-Domain Routing)** is the modern method of subnetting that uses **prefix notation** (e.g., `198.51.100.0/24`) for flexible IP address allocation.
- Subnetting improves network performance by keeping local traffic within the same subnet and reducing unnecessary network traffic.
- Organizations use subnetting to create **security zones**, isolate departments, enforce access controls, and limit the spread of cyberattacks.