# Public Key Infrastructure (PKI)

## What is Public Key Infrastructure?

**Public Key Infrastructure (PKI):** An encryption framework that secures the exchange of information online.

PKI provides a broad system for securely exchanging information between users, companies, computers, and networks. It helps address the challenge of protecting encryption keys and establishing trust between communicating parties.

PKI uses a **two-step approach**:

1. Exchange encrypted information using **asymmetric encryption, symmetric encryption, or both**.
2. Establish trust using **digital certificates**.

---

## Step 1: Exchange Encrypted Information

PKI can use both **asymmetric** and **symmetric encryption**.

### Asymmetric Encryption

**Asymmetric encryption:** An encryption method that uses a **public and private key pair** for encryption and decryption.

Think of it as a box with two different keys:

- **Public key:** Can be shared with others and used to send encrypted information to the owner.
- **Private key:** Kept secret by the owner and used to decrypt the information.

### How Asymmetric Encryption Works

1. The owner shares their **public key**.
2. Another person or server uses the public key to encrypt information.
3. The encrypted information is sent to the owner.
4. Only the corresponding **private key** can decrypt the information.

The public key can be widely distributed because it does not provide access to the private key.

**Advantages:**
- Provides a secure method for exchanging information.
- Helps establish secure communication without directly sharing a secret key.

**Disadvantage:**
- It is generally **slower** than symmetric encryption.

---

### Symmetric Encryption

**Symmetric encryption:** An encryption method that uses a **single secret key** for encryption and decryption.

Using the locked-box example, the same key can be used to:

- Lock the box.
- Add or access information.
- Unlock the box.

To communicate securely, the secret key must be shared with the other party.

**Advantages:**
- Faster than asymmetric encryption.
- Simpler approach to key management.

**Disadvantage:**
- Sharing the secret key creates a security risk because the key can be **misused, lost, or stolen**.

---

## Asymmetric vs. Symmetric Encryption

| Feature | Asymmetric Encryption | Symmetric Encryption |
|---|---|---|
| Keys used | Public and private key pair | Single secret key |
| Key sharing | Public key can be widely shared | Secret key must be shared securely |
| Speed | Slower | Faster |
| Security | More secure for establishing communication | Faster but depends heavily on protecting the secret key |
| Common use in PKI | Establishing secure connections | Fast communication after a connection is established |

### Using Both Encryption Methods

PKI can use **asymmetric and symmetric encryption together**.

For example, a mobile chat application may:

1. Use **asymmetric encryption** to establish a secure connection.
2. Switch to **symmetric encryption** for ongoing communication where speed is important.

This combines the security benefits of asymmetric encryption with the speed of symmetric encryption.

---

# Step 2: Establishing Trust

Both asymmetric and symmetric encryption have a common vulnerability:

> **How can computers know that they are communicating with a trusted party?**

Keys can be:

- Misused
- Lost
- Stolen

Humans can often use their senses and experience to determine whether someone is trustworthy. Computers do not naturally have this ability.

PKI addresses this problem through **digital certificates**.

---

## Digital Certificates

**Digital certificate:** A file that verifies the identity of a public key holder.

Digital certificates are commonly used when exchanging information online. They help users, companies, computers, and networks establish trust with one another.

A digital certificate acts similarly to an **online digital ID badge**. It can help verify the identity of the entity associated with a public key.

---

## Certificate Authority (CA)

**Certificate Authority (CA):** A trusted entity that verifies identities and issues digital certificates.

### Digital Certificate Creation Process

For example, an online business wants to launch a website and obtain a digital certificate.

1. The business registers its domain.
2. The hosting company sends information about the business to a trusted **Certificate Authority (CA)**.
3. The information may include details such as:
   - Company name
   - Country where the company headquarters are located
   - The website's public key
4. The CA verifies the company's identity.
5. After verification, the CA uses its **private key** to protect the verified certificate information.
6. The CA creates a **digital certificate** containing the relevant information and the CA's **digital signature**.
7. The digital signature helps prove that the certificate is authentic.

---

## Digital Signatures

A **digital signature** is included in a digital certificate to help demonstrate that the certificate was issued by the trusted Certificate Authority.

The CA uses its private key as part of the signing process. This allows others to verify the certificate using the CA's corresponding public key.

---

# How PKI Solves the Trust Problem

PKI combines:

- **Asymmetric encryption**
- **Symmetric encryption**
- **Digital certificates**
- **Certificate Authorities**
- **Digital signatures**

Together, these components allow computers and networks to establish trust while securely exchanging information.

### Simplified PKI Process

```text
1. Establish secure communication
          ↓
2. Use asymmetric encryption
          ↓
3. Establish trust using digital certificates
          ↓
4. Use symmetric encryption when speed is important
          ↓
5. Securely exchange information