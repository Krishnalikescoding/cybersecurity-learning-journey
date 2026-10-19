# Incident Lifecycle Frameworks

## Why frameworks matter

Incident lifecycle frameworks give structure to incident response, so incidents are handled in an **effective and consistent** way. Organizations can adopt a framework and modify it to fit their needs.

---

## NIST CSF (Cybersecurity Framework)

The five core functions:

1. **Identify**
2. **Protect**
3. **Detect**
4. **Respond**
5. **Recover**

This course focuses on the last three (**detect, respond, recover**). As an analyst, you'll detect and respond to incidents and carry out recovery actions.

---

## NIST incident response lifecycle

A separate NIST framework with extra substeps dedicated to incident response.

| Phase | Name |
|-------|------|
| 1 | Preparation |
| 2 | Detection and analysis |
| 3 | Containment, eradication, and recovery |
| 4 | Post-incident activity |

**Not linear.** It's a **cycle**, and phases can overlap as new discoveries are made.

---

## Events vs. incidents

> **All security incidents are events, but not all events are security incidents.**

| Term | Definition |
|------|-----------|
| **Event** | An observable occurrence on a network, system, or device |
| **Incident** (NIST) | An occurrence that actually or imminently jeopardizes, without lawful authority, the confidentiality, integrity, or availability of information or an information system; or constitutes a violation or imminent threat of violation of law, security policies, security procedures, or acceptable use policies |

### Example

| Scenario | Event? | Incident? |
|----------|:------:|:---------:|
| A user forgets their password, requests a reset, and changes it | Yes | No |
| A malicious actor requests a reset and changes the password on an account that isn't theirs | Yes | Yes |

- The first is logged and shows no policy was violated.
- The second is still an observable event, but it's also an incident because a security policy was violated to gain unlawful access.

---

## Documenting an investigation

Analysts must carefully handle and document evidence and findings, much like detectives working a case.

### The five W's

| Question | Asks |
|----------|------|
| **Who** | Who triggered the incident |
| **What** | What happened |
| **When** | When it took place |
| **Where** | Where it took place |
| **Why** | Why it occurred |

Tracking this matters during the investigation **and** at closure, when you write the final report.

### Incident handler's journal

A form of documentation used in incident response. You'll keep your own throughout the course to record incident details.

---

## Quick recall

- **CSF functions to focus on:** detect, respond, recover
- **NIST IR lifecycle:** preparation, detection and analysis, containment/eradication/recovery, post-incident activity
- **Lifecycle shape:** a cycle, not a straight line
- **Event vs. incident:** every incident is an event, but not every event is an incident
- **Five W's:** who, what, when, where, why