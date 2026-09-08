# Software Updates & Patching 

## Why Updates Matter
- Improve performance, stability, features (consumer side).
- Security side: fix vulnerabilities that put users, devices, networks at risk.
- Typically happen after a vulnerability assessment, as part of remediation strategy.

## Patches
- **Patch update**: software/OS update that fixes security vulnerabilities in a program/product.
- Usually address known vulnerabilities and exposures.
- Sometimes created in response to a **zero-day** (a previously unknown exploit).

## Update Deployment Strategies

### Manual Updates
- IT/users get updates themselves; enterprises often use configuration management tools to control rollout (all clients or select groups).
- **Advantage**: more control — useful if updates aren't well-tested and could cause instability.
- **Disadvantage**: critical updates can be forgotten/ignored.

### Automatic Updates
- System/application finds, downloads, installs updates itself.
- CISA recommends automatic updates when available.
- Requires certain permissions enabled beforehand; relies on vendor testing patches properly.
- **Advantage**: simplified process, keeps systems current with critical patches.
- **Disadvantage**: instability risk if vendor didn't test thoroughly → performance/user experience issues.

## End-of-Life (EOL) Software
- Every software has a lifecycle: created → superseded by newer version → EOL.
- EOL = manufacturer no longer supports/updates it, even though still usable.
- **Patches/updates ≠ upgrades** (upgrades = new purchased versions of hardware/software).
- CISA recommends discontinuing EOL software (unfixable risk) — but not always followed due to replacement costs.
- Risk grows with more connected/IoT devices (e.g., smart bulbs); one unpatched device can expose a whole network.

## Key Takeaways
- Keeping software updated is essential but often neglected.
- **Example**: WannaCry attack (2017) — hit 150+ countries, ~$4 billion in damages — preventable via a patch that had been available months earlier.
- Updating requires effort, but benefits outweigh the cost.