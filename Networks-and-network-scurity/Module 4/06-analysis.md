# Network Hardening Security Risk Assessment

## Activity Overview

In this activity, a social media organization has experienced a major data breach caused by undetected vulnerabilities.

The objective is to:

- Identify common network hardening tools and methods.
- Identify vulnerabilities within the organization's network.
- Select up to three hardening methods to address the vulnerabilities.
- Explain how the selected methods can improve network security.
- Explain how the recommendations can help prevent future breaches.

Network hardening practices help organizations monitor potential threats and attacks while preventing some attacks from occurring.

Examples of network hardening practices include:

- Port filtering
- Network access privileges
- Encryption over networks
- Strong authentication
- Password policies
- Firewall maintenance

Some hardening practices are performed regularly, while others may be performed periodically, such as every few weeks or once a month.

---

## Scenario

You are a security analyst working for a social media organization.

The organization recently experienced a major data breach that compromised customers' personal information, including:

- Names
- Addresses

After inspecting the organization's network, you identified four major vulnerabilities.

### Identified Vulnerabilities

1. **Employees share passwords.**
2. **The database administrator password is set to the default password.**
3. **Firewalls do not have rules configured to filter incoming and outgoing traffic.**
4. **Multi-factor authentication (MFA) is not used.**

If these vulnerabilities are not addressed, the organization remains at risk of additional data breaches and other attacks.

The purpose of the assessment is to analyze the security risks and recommend network hardening methods that can improve the organization's security.

---

# Part 1: Hardening Tools and Methods

Up to three hardening tools and methods can be implemented to address the identified vulnerabilities.

### Recommended Methods

1. **Implement Multi-Factor Authentication (MFA)**
2. **Establish and enforce strong password policies**
3. **Perform regular firewall maintenance**

---

## 1. Multi-Factor Authentication (MFA)

**Multi-Factor Authentication (MFA):** An authentication method that requires users to provide more than one form of identification or verification before accessing an application or system.

Examples of MFA methods include:

- Fingerprint scans
- ID cards
- PIN numbers
- Passwords

MFA adds an additional layer of security beyond a password.

---

## 2. Strong Password Policies

A **password policy** establishes rules that users must follow when creating and using passwords.

Password policies can define:

- Minimum password length
- Acceptable characters
- Restrictions against password sharing
- Rules for unsuccessful login attempts
- Password reuse restrictions
- Password update requirements
- Account suspension after a specified number of unsuccessful login attempts

For example, an organization could suspend an account after five unsuccessful login attempts.

Strong password policies make it more difficult for malicious actors to gain unauthorized access to systems.

---

## 3. Regular Firewall Maintenance

**Firewall maintenance** involves regularly checking and updating firewall security configurations to remain prepared for potential threats.

Firewall maintenance can include reviewing and updating rules that control:

- Incoming network traffic
- Outgoing network traffic

Properly configured firewall rules can help filter unwanted or unauthorized traffic.

Regular maintenance ensures that firewall configurations remain appropriate as security requirements and potential threats change.

---

# Part 2: Recommendations

## Implement Multi-Factor Authentication

Enforcing MFA adds an additional layer of security beyond a password.

MFA can reduce the likelihood that a malicious actor successfully accesses the network through a brute-force or related attack because the attacker must successfully complete more than one authentication method.

MFA can also reduce the usefulness of password sharing. If a shared password is not sufficient to access the system, the person receiving the password would still need the additional authentication factor.

Therefore, MFA can:

- Add another layer of authentication.
- Make unauthorized access more difficult.
- Reduce the effectiveness of stolen or shared passwords.
- Help protect accounts against brute-force attacks.

---

## Create and Enforce a Password Policy

Creating and enforcing a strong password policy makes unauthorized access more difficult for malicious actors.

Useful password policy requirements include:

- Increasing password complexity.
- Requiring regular password updates.
- Preventing password reuse.
- Restricting password sharing.
- Suspending accounts after a specified number of unsuccessful login attempts.

For example, temporarily suspending an account after multiple failed login attempts can help prevent successful brute-force attacks.

A strong password policy directly addresses the vulnerability of employees sharing passwords and can also improve protection against unauthorized account access.

---

## Perform Regular Firewall Maintenance

Regular firewall maintenance helps ensure that firewall security configurations remain effective against potential threats.

The organization should regularly review and update firewall rules to filter traffic entering and leaving the network.

Proper firewall configuration can help:

- Control incoming traffic.
- Control outgoing traffic.
- Filter unauthorized or unwanted network traffic.
- Strengthen the organization's network security.

Regular maintenance is important because firewall configurations must remain aligned with the organization's security requirements.

---

# Security Risk Assessment Summary

The organization has several vulnerabilities that could contribute to another data breach if they remain unresolved.

| Vulnerability | Recommended Hardening Method |
|---|---|
| Employees share passwords | MFA and strong password policies |
| Database administrator uses the default password | Strong password policies |
| Firewalls lack traffic-filtering rules | Regular firewall maintenance |
| MFA is not implemented | Implement MFA |

The selected hardening methods provide multiple layers of protection. MFA strengthens authentication, password policies improve password security and account protection, and firewall maintenance improves network traffic filtering.

---

# Key Takeaways

- **Network hardening** uses security tools and practices to strengthen an organization's network.
- The organization in this scenario has four major vulnerabilities involving password sharing, a default database password, ineffective firewall rules, and the absence of MFA.
- **MFA** adds an additional authentication layer and can reduce the effectiveness of stolen or shared passwords.
- **Strong password policies** can improve password security and help defend against brute-force attacks.
- **Regular firewall maintenance** helps ensure that incoming and outgoing traffic is properly filtered.
- Combining multiple hardening methods provides layered protection against potential attacks and future data breaches.