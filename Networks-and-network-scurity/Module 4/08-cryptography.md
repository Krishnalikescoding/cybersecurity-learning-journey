# Cloud Security Hardening and Cryptography

## Overview

Cloud networks, like on-premises networks, require a combination of **security hardening practices** and **cryptography** to protect infrastructure, resources, and data.

Common cloud security hardening techniques include:

- **Identity and Access Management (IAM)**
- **Hypervisor security**
- **Baselining**
- **Cryptography**
- **Cryptographic erasure**
- **Key management**

Understanding these practices is important as cloud infrastructure becomes increasingly common.

## Cloud Security Hardening

**Cloud security hardening** involves using security techniques and tools to strengthen cloud infrastructure and reduce security risks.

Common hardening practices include:

- Implementing IAM
- Securing hypervisors
- Establishing configuration baselines
- Using cryptography
- Using cryptographic erasure
- Protecting encryption keys

## Identity and Access Management (IAM)

**Identity and Access Management (IAM):** A collection of processes and technologies used to manage digital identities and authorize how users can access and use cloud resources.

IAM helps organizations control access to cloud resources and prevent unauthorized use.

## Hypervisors

A **hypervisor** abstracts the host computer's hardware from the operating software environment, allowing multiple virtual machines (VMs) to operate on the same physical hardware.

There are two main types of hypervisors:

| Type | Description | Example |
|---|---|---|
| **Type 1** | Runs directly on the host computer's hardware | VMware ESXi |
| **Type 2** | Runs on the host computer's operating system | VirtualBox |

### Hypervisors in the Cloud

Cloud Service Providers (CSPs) commonly use **Type 1 hypervisors**.

The CSP is responsible for managing:

- Hypervisors
- Virtualization components
- Patches and updates
- Availability of cloud resources and environments

Vulnerabilities or misconfigurations in hypervisors can result in **Virtual Machine (VM) escapes**.

**VM Escape:** An exploit in which a malicious actor gains access from a virtual machine to the underlying hypervisor, potentially allowing access to the host computer and other virtual machines.

Cloud customers generally do not interact directly with the underlying hypervisors.

## Baselining

**Baseline:** A fixed reference point used to compare changes made to a system or environment.

**Cloud baselining** defines how a cloud environment should be configured and set up. Comparing the current environment against the baseline can help identify configuration changes or security issues.

Proper configuration and setup can improve:

- Security
- Performance
- Consistency of the cloud environment

### Examples of Cloud Baseline Configuration

Examples include:

- Restricting access to the cloud administration portal
- Enabling password management
- Enabling file encryption
- Enabling threat detection services for SQL databases

## Cryptography in the Cloud

**Cryptography** can be used to protect data that is processed and stored in cloud environments.

Cryptography uses techniques such as **encryption** and secure **key management** to help provide:

- **Confidentiality**
- **Integrity**

### Encryption

**Encryption:** The process of transforming readable information into **ciphertext**, making it unreadable without the appropriate encryption key.

Traditional encryption methods often relied on algorithms that manually transformed letters or numbers into different values.

Modern encryption primarily relies on the **secrecy of the encryption key**, rather than keeping the encryption algorithm secret.

Encryption is an important method for protecting sensitive cloud data and data at rest from unauthorized access.

## Cryptographic Erasure

**Cryptographic erasure:** A method of destroying encrypted data by securely destroying the encryption key required to decrypt it.

Traditional methods of destroying data may be less effective in cloud environments because multiple copies of data may exist.

### Crypto-Shredding

**Crypto-shredding** is a technique in which the cryptographic keys used to decrypt data are destroyed.

Once the keys are destroyed:

- The encrypted data becomes undecipherable.
- The data can no longer be decrypted using the destroyed keys.
- All copies of the relevant keys must be destroyed to prevent future access.

## Key Management

Modern encryption depends on keeping encryption keys secure.

Two technologies that can help protect cryptographic keys are:

### Trusted Platform Module (TPM)

**Trusted Platform Module (TPM):** A computer chip designed to securely store sensitive information such as:

- Passwords
- Certificates
- Encryption keys

### Cloud Hardware Security Module (CloudHSM)

**Cloud Hardware Security Module (CloudHSM):** A computing device that provides secure storage for cryptographic keys and performs cryptographic operations such as:

- Encryption
- Decryption

## Cloud Provider and Customer Key Responsibilities

Organizations and customers generally do not have direct access to the CSP's infrastructure. However, they can request audits and security reports from the CSP.

Customers typically do not have access to the specific encryption keys that CSPs use to encrypt customer data.

Depending on the cloud service, many CSPs allow customers to provide and manage their own encryption keys.

When customers provide their own keys, they become responsible for:

- Protecting the keys
- Maintaining key confidentiality
- Preventing unauthorized access
- Handling compromised or destroyed keys

If customer-managed keys are compromised or destroyed, the CSP may have limited ability to recover or assist with the affected data.

### Shared Responsibility and Cryptographic Infrastructure

The **shared responsibility model** means that customers do not necessarily have to maintain the entire underlying cryptographic infrastructure themselves.

Organizations can evaluate the risks associated with allowing a CSP to manage cryptographic infrastructure by reviewing:

- CSP audits
- Security reports
- Security controls

For federal contractors, **FedRAMP (Federal Risk and Authorization Management Program)** provides a list of verified CSPs.

## Key Takeaways

- Cloud networks require security hardening just like on-premises networks.
- **IAM** controls identities and access to cloud resources.
- CSPs commonly use **Type 1 hypervisors**, which they are responsible for managing and patching.
- Hypervisor vulnerabilities or misconfigurations can lead to **VM escapes**.
- **Baselines** provide a fixed reference point for comparing changes to cloud configurations.
- **Cryptography** helps protect the confidentiality and integrity of cloud data.
- **Encryption** transforms plaintext into ciphertext that requires an encryption key to decrypt.
- **Cryptographic erasure** and **crypto-shredding** destroy encryption keys to make encrypted data undecipherable.
- **TPMs** and **CloudHSMs** can provide secure storage and management of cryptographic keys.
- Customers using their own encryption keys are responsible for protecting and maintaining those keys.
- The **shared responsibility model** determines how security and cryptographic responsibilities are divided between the CSP and customer.