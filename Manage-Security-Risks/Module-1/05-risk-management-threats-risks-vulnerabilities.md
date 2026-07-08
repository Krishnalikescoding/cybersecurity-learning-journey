# Risk Management, Threats, Risks, and Vulnerabilities

Organizations protect their **assets** by identifying, assessing, and managing **threats, risks, and vulnerabilities**. Understanding the current threat landscape helps organizations develop policies and processes to prevent and reduce security incidents.

---

# Risk Management

**Risk management** is the process of identifying, assessing, and reducing risks to an organization's assets.

## Assets

An **asset** is anything that has value to an organization.

### Digital Assets
- Social Security Numbers (SSNs) / National ID numbers
- Dates of birth
- Bank account numbers
- Mailing addresses
- Employee, customer, and vendor data

### Physical Assets
- Payment kiosks
- Servers
- Desktop computers
- Office spaces

---

# Risk Management Strategies

Organizations commonly use four strategies to manage risk.

## 1. Acceptance
Accept a risk because avoiding or reducing it would cost more than the potential impact.

## 2. Avoidance
Eliminate the activity or process that creates the risk.

## 3. Transference
Transfer the risk to a third party (e.g., insurance providers or managed security services).

## 4. Mitigation
Reduce the likelihood or impact of a known risk by implementing security controls.

---

# Risk Management Frameworks

Organizations use industry-standard frameworks to manage cybersecurity risks.

## NIST Risk Management Framework (NIST RMF)
A framework developed by NIST to identify, assess, and manage security and privacy risks.

## HITRUST
A security framework designed primarily for protecting healthcare information and ensuring regulatory compliance.

---

# Common Threats

A **threat** is any event or circumstance that can negatively affect an organization's assets.

## Insider Threats
Employees, contractors, or vendors misuse their authorized access to steal, modify, or expose organizational data.

## Advanced Persistent Threats (APTs)
A threat actor gains unauthorized access to a system and remains undetected for a long period while collecting information or causing damage.

---

# Risks

A **risk** is anything that can impact the **Confidentiality, Integrity, or Availability (CIA)** of an asset.

**Risk = Likelihood that a threat will exploit a vulnerability.**

## Common Types of Risks

### External Risk
Threats originating outside the organization.

**Examples**
- Hackers
- Malware
- Cyberattacks
- Data breaches

---

### Internal Risk
Security risks caused by trusted individuals.

**Examples**
- Employees
- Former employees
- Vendors
- Business partners

---

### Legacy Systems
Outdated hardware or software that is still in use but no longer receives security updates.

**Examples**
- Old workstations
- Legacy accounting systems
- Network-connected payment kiosks

---

### Multiparty Risk
Risks introduced by third-party vendors or contractors who have access to organizational systems or intellectual property.

---

### Software Compliance and Licensing Risk
Risks caused by:
- Outdated software
- Missing security patches
- Unsupported applications
- Licensing non-compliance

---

# OWASP Top 10

The **Open Web Application Security Project (OWASP)** publishes the **Top 10 Web Application Security Risks**, which are updated regularly to reflect evolving threats.

### New Risks Added (2017 → 2021)
- Insecure Design
- Software and Data Integrity Failures
- Server-Side Request Forgery (SSRF)

These updates highlight the importance of staying current with cybersecurity threats and attack techniques.

---

# Vulnerabilities

A **vulnerability** is a weakness that attackers can exploit.

Organizations should continuously monitor systems and apply security patches to reduce vulnerabilities.

## Common Vulnerabilities

### ProxyLogon
- A pre-authentication vulnerability affecting Microsoft Exchange Server.
- Allows attackers to execute malicious code remotely.

---

### ZeroLogon
- A vulnerability in Microsoft's Netlogon authentication protocol.
- Allows attackers to bypass authentication and gain unauthorized access.

---

### Log4Shell
- A critical vulnerability in Java applications using Log4j.
- Allows remote attackers to execute malicious code or access sensitive information.

---

### PetitPotam
- Targets Windows NTLM authentication.
- Forces authentication requests that attackers can exploit.

---

### Security Logging and Monitoring Failures
- Insufficient logging or monitoring prevents organizations from detecting attacks promptly.

---

### Server-Side Request Forgery (SSRF)
- Tricks a server into sending requests to internal or external resources.
- Can lead to unauthorized access and data theft.

---

# Vulnerability Management

**Vulnerability management** is the continuous process of identifying, assessing, and reducing vulnerabilities within organizational systems.

## Responsibilities of a Security Analyst

- Monitor systems for vulnerabilities
- Apply security patches and updates
- Verify systems remain secure
- Reduce exposure to known vulnerabilities
- Continuously assess organizational security

Timely patching and monitoring significantly reduce the chances of successful cyberattacks.

---

# Resources

Useful resources for researching vulnerabilities:

- **NIST National Vulnerability Database (NVD)**
- **CISA Known Exploited Vulnerabilities Catalog**
- **OWASP Top 10**

---

# Key Takeaways

- **Risk management** helps organizations protect valuable assets.
- Assets can be **digital** or **physical**.
- Four risk management strategies are:
  - Acceptance
  - Avoidance
  - Transference
  - Mitigation
- Common threats include **Insider Threats** and **Advanced Persistent Threats (APTs)**.
- Common risks include:
  - External risks
  - Internal risks
  - Legacy systems
  - Multiparty risks
  - Software compliance risks
- Common vulnerabilities include:
  - ProxyLogon
  - ZeroLogon
  - Log4Shell
  - PetitPotam
  - Security logging and monitoring failures
  - Server-Side Request Forgery (SSRF)
- Continuous vulnerability management, monitoring, and patching are essential for reducing organizational risk.