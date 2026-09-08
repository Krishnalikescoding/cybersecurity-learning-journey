# Penetration Testing

## Penetration Testing

- **Penetration test (pen test):** A simulated, authorized attack used to identify and exploit vulnerabilities.
- Tests can target:
  - Systems
  - Networks
  - Websites
  - Applications
  - Processes
- Uses tools and techniques similar to those used by **malicious actors**.
- Considered a form of **ethical hacking** because the attack is authorized.
- Unlike a **vulnerability assessment**, a pen test:
  - Exploits identified weaknesses.
  - Determines the potential consequences of a successful attack.

### Example

- A financial company may simulate an attack on its banking app.
- The goal could be to find weaknesses that allow attackers to:
  - Steal customer information.
  - Illegally transfer funds.
- **Misconfigurations** found during testing can be fixed to improve security.

### Compliance

- Organizations regulated by the following may need routine penetration testing:
  - **PCI DSS**
  - **HIPAA**
  - **GDPR**

## Red, Blue, and Purple Team Testing

- **Red team:**
  - Simulates attacks.
  - Identifies vulnerabilities in systems, networks, and applications.

- **Blue team:**
  - Focuses on defense and **incident response**.
  - Tests the effectiveness of existing security systems.

- **Purple team:**
  - Combines red and blue team activities.
  - Uses collaboration to improve the organization's **security posture**.

- Pen testers must decide how much **access and information** they need before testing.

## Penetration Testing Strategies

### Open-Box Testing

- Tester has **privileged access** similar to an internal developer.
- May receive:
  - System architecture
  - Data flow
  - Network diagrams
- Also called:
  - **Internal testing**
  - **Full knowledge testing**
  - **White-box testing**
  - **Clear-box testing**

### Closed-Box Testing

- Tester has **little or no internal access**.
- Simulates the position of a malicious hacker.
- Also called:
  - **External testing**
  - **Black-box testing**
  - **Zero-knowledge testing**
- Usually produces the most accurate simulation of a **real-world attack**.

### Partial Knowledge Testing

- Tester has **limited access and knowledge**.
- Example: Access similar to a **customer service representative**.
- Also called **gray-box testing**.

- Each strategy helps show:
  - How an attacker could infiltrate a system.
  - What information the attacker could access.

## Skills for Penetration Testing

- **Network and application security**
- **Operating systems**, such as Linux
- **Vulnerability analysis**
- **Threat modeling**
- **Detection and response tools**
- **Programming**, including:
  - Python
  - BASH
- **Communication skills**

- Programming is especially useful because pen testing often targets software and IT systems.
- Cybersecurity professionals at different skill levels can develop into penetration testers with practice and dedication.

## Bug Bounty Programs

- **Bug bounty programs:** Programs that reward freelance pen testers for finding and reporting vulnerabilities.
- Provide opportunities for:
  - Amateur security professionals
  - Skill development
  - Practical security experience
- **[HackerOne](https://hackerone.com/bug-bounty-programs)** provides a community for ethical hackers and lists active bug bounty programs.

## Key Takeaways

- **Penetration testing** uses simulated attacks to identify and exploit security weaknesses.
- It helps organizations understand the potential impact of vulnerabilities.
- **Red teams** focus on attacking.
- **Blue teams** focus on defense and incident response.
- **Purple teams** combine red and blue team activities.
- Common testing strategies:
  - **Open-box**
  - **Closed-box**
  - **Partial knowledge / gray-box**
- Penetration testing is an in-demand cybersecurity field.
- Skills in networking, Linux, vulnerability analysis, programming, and communication can help build a career in pen testing.
- **Bug bounty programs** provide opportunities to practice finding and reporting vulnerabilities.