# Introduction to Package Managers

## Overview
A **package** is a piece of software that can be combined with other packages to form an application, though some packages are large enough to function as standalone applications. Packages contain all the files required to install an application, including **dependencies**—supplemental files and libraries needed to run the software properly.

A **package manager** is a tool that helps users install, configure, update, and remove packages or applications, as well as resolve dependency conflicts.

> **Security Note:** Always use the most recent version of a package when possible. Up-to-date versions contain the latest bug fixes and security patches, which minimize vulnerabilities and help secure the system.

---

## Package Managers by Linux Distribution

Linux distributions derived from different parent operating systems use specific package managers and packaging formats.

| Parent Distribution | Example Derivative Distributions | Package Manager | Package File Extension | Naming Convention Example |
| :--- | :--- | :--- | :--- | :--- |
| **Debian** | Kali Linux, Ubuntu, Parrot OS | `dpkg` | `.deb` | `Package_Version-Release_Architecture.deb` |
| **Red Hat** | CentOS | Red Hat Package Manager (`RPM`) | `.rpm` | `Package-Version-Release_Architecture.rpm` |

---

## Package Management Tools

While low-level package managers like `dpkg` and `RPM` handle local package files directly, higher-level **package management tools** interact with remote repositories through the command-line interface (CLI) to automate tasks like dependency resolution, searching, downloading, and installing packages.

### Advanced Package Tool (APT)
- Used with **Debian-derived** distributions (e.g., Debian, Ubuntu, Kali Linux, Parrot OS).
- Executed via the CLI to search, install, update, and manage `.deb` packages.

### Yellowdog Updater, Modified (YUM)
- Used with **Red Hat-derived** distributions (e.g., Red Hat Enterprise Linux, CentOS).
- Executed via the CLI to search, install, update, and manage `.rpm` packages.

---

## Key Takeaways

- **Packages & Dependencies:** Packages contain the application files and dependencies required for software to execute.
- **Security Best Practice:** Keeping packages updated ensures systems receive critical security patches and vulnerability fixes.
- **Ecosystem Differences:** 
  - **Debian family** uses `dpkg` (package manager), `.deb` files, and `APT` (front-end CLI tool).
  - **Red Hat family** uses `RPM` (package manager), `.rpm` files, and `YUM` (front-end CLI tool).