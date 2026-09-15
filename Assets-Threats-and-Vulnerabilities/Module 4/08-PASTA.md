# PASTA Threat Modeling Framework 

## What is PASTA?
- **PASTA** = Process for Attack Simulation and Threat Analysis.
- A popular threat modeling framework used across many industries.
- Illustrated using example: a fitness company launching a mobile app that needs to protect customer data.

## The 7 Stages of PASTA

### Stage 1: Define Business & Security Objectives
- Team decides on goals before starting (e.g., protecting customer data).
- Involves asking key questions, like how personally identifiable information (PII) is handled.
- Answers here help evaluate the impact of threats found later.

### Stage 2: Define the Technical Scope
- Identify application components that must be evaluated (i.e., the **attack surface**).
- For a mobile app: includes tech involved when data is **at rest** and **in use** — network protocols, security controls, data interactions.

### Stage 3: Decompose the Application
- Identify existing controls protecting user data from threats.
- Typically done by working with developers to create a **data flow diagram**.
- Diagram shows how data moves from user device → company database, plus controls along the way.

### Stage 4: Perform Threat Analysis
- Team applies an attacker mindset.
- Research current, up-to-date attack trends/techniques.
- Attack vectors for mobile apps change regularly — requires staying current with resources.

### Stage 5: Perform Vulnerability Analysis
- Deeper investigation into potential vulnerabilities.
- Focus on identifying the **root cause** of each problem.

### Stage 6: Conduct Attack Modeling
- Test vulnerabilities identified in Stage 5 by simulating attacks.
- Done using an **attack tree** (flow-chart style diagram).
- Example: customer usernames/passwords (target) → stored in database → vulnerable to **SQL injection** via unsanitized inputs → added as a branch on the attack tree.
- Real apps typically have many branches covering multiple attack vectors.

### Stage 7: Analyze Risk & Impact
- Team compiles everything gathered across Stages 1–6.
- Produces informed risk management recommendations for business stakeholders, aligned with original objectives.

## Key Takeaways
- PASTA is a structured, 7-stage process moving from defining objectives → technical scope → app decomposition → threat analysis → vulnerability analysis → attack modeling → risk/impact analysis.
- Ends with actionable, business-aligned risk recommendations.