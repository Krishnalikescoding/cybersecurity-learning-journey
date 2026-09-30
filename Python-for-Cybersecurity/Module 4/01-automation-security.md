# Automating Security in CI/CD with Python

## Core Idea
- **CI/CD** = Continuous Integration and Continuous Delivery/Deployment.
- **DevSecOps** = Development + Security + Operations working together from the start.
- Security is a shared responsibility, built into the pipeline, not added at the end.
- Python is used to run security checks automatically inside the pipeline.

## Why Use Python?
Doing checks by hand is slow and error-prone. Python is flexible and has many libraries.

| Benefit | Meaning |
|---|---|
| Speed and efficiency | Fast scripts, releases stay quick and secure |
| Finds problems early | Cheaper and easier to fix |
| Consistency | Same checks every build, less human error |
| Less workload for security teams | Frees them for bigger problems |
| Security culture | Everyone thinks about security, not just the security team |

## Security Tasks Python Can Automate

### 1. Security Testing
- **SAST** (Static Application Security Testing): scans code for weaknesses before it is built. Python triggers the tool, reads results, makes reports, and can stop the pipeline on serious issues.
- **DAST** (Dynamic Application Security Testing): tests the software while it runs in a test environment. Python runs the tool and feeds results back into the pipeline.
- **SCA** (Software Composition Analysis): checks dependencies (open source code, third-party components) for weaknesses. Python controls the process and sets rules based on severity.

### 2. Automated Vulnerability Scanning
- Covers container images, infrastructure settings, and the pipeline itself.
- Python schedules scans, collects results, and sends alerts for new vulnerabilities.

### 3. Compliance Checks
- Checks that code follows secure coding rules.
- Checks that infrastructure settings meet security guidelines.
- Python generates compliance reports.

### 4. Secrets Management
- Scans code to stop credentials from being hard-coded.
- Works with tools like **HashiCorp Vault** to fetch and inject secrets safely during releases.

### 5. Policy Enforcement
- **Policy as Code**: policies are defined in code, and Python checks pipeline steps against them.
- Example: too many vulnerabilities found, so Python stops the release.

## How Python Fits with CI/CD Tools
Works with **Jenkins, GitLab CI, CircleCI**.
- **Run scripts**: pipeline steps can run Python scripts directly.
- **APIs**: Python is good at calling APIs, so it can manage the pipeline, start jobs, fetch build files, and trigger scans on security tools.
- **Add-ons/extensions**: some CI/CD systems have plugins written in Python or that run Python easily.

## Other CI/CD Tasks Python Can Help With
- **Set up environments**: build staging areas with secure network settings and controls.
- **Code quality checks**: run linters for style problems and possible security errors early.
- **Secure releases**: automate releases to staging and production, using secure settings and safe file transfer.

## Key Takeaways
- Automating security in CI/CD is now a must, not a nice-to-have.
- DevSecOps means security is built in, not added later.
- Python gives a pipeline that is faster, more efficient, and more secure.

## Next Topics (in the course)
Variables, conditional statements, iterative statements (loops), functions, and working with files. These are the basic building blocks for writing security automation scripts.

## Quick Memory Hook
**SAST** = scan code (static) | **DAST** = test running app | **SCA** = check dependencies

## Resources
- Best Python Libraries for Cybersecurity in 2024: https://medium.com/@Scofield_Idehen/best-python-libraries-for-cybersecurity-in-2024-037a870f39d1
- Vulnerability Scanning for Secure Python Development: https://www.getsafety.com/
- OWASP Dependency-Check and Vulnerability Scanning: https://www.linkedin.com/pulse/article-3-owasp-dependency-check-vulnerability-scanning-adorsys-p73fe
- Python library for HashiCorp Vault: https://discuss.hashicorp.com/t/python-library-for-hashicorp-vault-implementation/55805
- Continuous Integration With Python (Real Python): https://realpython.com/python-continuous-integration/
- Python for DevOps: An Ultimate Guide: https://code-b.dev/blog/python-devops
- Building Custom Cybersecurity Tools with Python: https://www.linkedin.com/pulse/building-custom-cybersecurity-tools-python-bi6if
- Secure Coding in Python for Data Engineers: https://www.linkedin.com/pulse/secure-coding-python-essential-practices-data-engineers-priyanka-sain-wewkc