# Threat Modeling 

## What is Threat Modeling?
- **Threat modeling**: process of identifying assets, their vulnerabilities, and how each is exposed to threats.
- Applied to systems, applications, and business processes.
- Considered an **advanced security skill** — usually performed by experienced professionals, though analysts can still be involved.
- Attacks vary by target (e.g., small business vs. public utility) — different assets, different defenses needed.
- Several frameworks exist, suited for different contexts (network security, information security, app development).

## The 6 Steps of Threat Modeling

### 1. Define the Scope
- Determine what's being built/protected.
- Create an inventory of assets and classify them.

### 2. Identify Threats
- Define all potential threat actors.
- **Threat actor**: any person/group posing a security risk.
  - **Internal** – e.g., an employee intentionally exposing an asset
  - **External** – e.g., a malicious hacker or competing business
- Build an **attack tree** – a diagram mapping threats to assets (as detailed as possible).

### 3. Characterize the Environment
- Apply an attacker mindset to the business.
- Consider how customers and employees interact with the environment.
- Also factor in external partners and third-party vendors.

### 4. Analyze Threats
- Examine existing protections and identify gaps.
- Rank threats using an assigned **risk score**.

### 5. Mitigate Risk
- Create a plan for defending against threats.
- Choices: **avoid**, **transfer**, **reduce**, or **accept** the risk.

### 6. Evaluate Findings
- Document everything done during the exercise.
- Apply fixes.
- Note successes and lessons learned to inform future threat models.

## Key Takeaways
- Threat modeling is a structured, team-based process for anticipating attacks.
- Six-step process: scope → identify threats → characterize environment → analyze threats → mitigate risk → evaluate findings.