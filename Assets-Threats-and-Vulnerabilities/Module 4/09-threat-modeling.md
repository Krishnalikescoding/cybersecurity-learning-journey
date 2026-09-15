# Application Security & Threat Modeling Frameworks – Notes

## Threat Modeling Recap
- Process of identifying assets, their vulnerabilities, and how each is exposed to threats.
- Combines multiple security activities: vulnerability management, threat analysis, incident response.
- Used to proactively reduce risk to systems or business processes.
- Traditionally tied to **application development**.

## Why Application Security Matters
- Web/mobile apps are central to how businesses connect with customers, partners, and each other.
- Smartphones are now a primary channel for data exchange → huge volume of data at risk.
- **Example**: **Log4Shell vulnerability ([CVE-2021-44228](https://nvd.nist.gov/vuln/detail/CVE-2021-44228))** in Java-based logging libraries.
  - If unpatched, allows **remote code execution** — attacker could gain full system access remotely.
  - Critical vulnerabilities like this can impact **millions of devices**.

## Defending the Application Layer
- Requires proper testing to uncover weaknesses.
- Usually performed by a **DevSecOps** team (Development, Security, Operations).
- Threat modeling cycle (6 steps): 
  1. Define the scope
  2. Identify threats
  3. Characterize the environment
  4. Analyze threats
  5. Mitigate risks
  6. Evaluate findings
- Ideally done **before, during, and after** development — but takes significant time/resources.
- Should be incorporated at every stage of the **Software Development Lifecycle (SDLC)**.

## Common Threat Modeling Frameworks

### STRIDE
- Developed by **Microsoft**.
- Identifies vulnerabilities across **six attack vectors** (the acronym):
  - **S**poofing
  - **T**ampering
  - **R**epudiation
  - **I**nformation disclosure
  - **D**enial of service
  - **E**levation of privilege

### PASTA
- **P**rocess for **A**ttack **S**imulation and **T**hreat **A**nalysis.
- Risk-centric approach, developed by two OWASP leaders, supported by cybersecurity firm **VerSprite**.
- Focus: discover evidence of viable threats, represent as a model.
- Can be applied to an application itself or its surrounding environment.
- 7-stage process incorporating security artifacts (e.g., vulnerability assessment reports).

### Trike
- **Open-source** methodology and tool.
- Security-centric approach.
- Focus areas: security permissions, application use cases, privilege models.

### VAST
- **V**isual, **A**gile, and **S**imple **T**hreat modeling.
- Part of the automated platform **ThreatModeler®**.
- Used to automate and streamline threat modeling assessments.

- **Note**: No single "right" framework — choice depends on situation and the specific risks an application faces.

## Participating in Threat Modeling
- Usually led by experienced professionals, but done as a **team effort** — especially for complex applications.
- Key questions to guide the process:
  1. What are we working on?
  2. What can go wrong?
  3. What are we doing about it?
  4. Have we addressed everything?
  5. Did we do a good job?
- Skills like data flow diagrams and attack trees take practice — but **anyone can learn** to contribute.

## Key Takeaways
- Securing applications is increasingly critical as reliance on software grows.
- Threat modeling helps verify security controls protect data privacy.
- Even less-experienced analysts can meaningfully contribute — it starts with an attacker mindset and critical thinking about data handling.