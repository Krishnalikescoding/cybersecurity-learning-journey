# Cloud Computing and Cloud Security

## Overview

**Cloud computing** is defined by the United Kingdom's National Cyber Security Centre (NCSC) as:

> "An on-demand, massively scalable service, hosted on shared infrastructure, accessible via the internet."

Cloud computing has changed how businesses operate by making it easier to scale, adapt, and provide online services. However, moving data, applications, and infrastructure to the cloud also introduces new cybersecurity challenges.

## Cloud-Based Services

**Cloud-based services** are on-demand or web-based business solutions that can range from website hosting and application development environments to complete back-end infrastructure.

There are three main categories:

1. **Software as a Service (SaaS)**
2. **Platform as a Service (PaaS)**
3. **Infrastructure as a Service (IaaS)**

### Software as a Service (SaaS)

**SaaS** provides front-end applications that users access through a web browser.

The cloud service provider hosts, manages, and maintains the back-end systems required to operate the application.

**Examples:**

- Gmail
- Slack
- Zoom

### Platform as a Service (PaaS)

**PaaS** provides online back-end application development tools.

Developers use these resources to:

- Write code
- Build applications
- Manage applications
- Deploy applications

The cloud service provider hosts and maintains the underlying hardware and software required for the applications to operate.

**Examples:**

- Google App Engine
- Heroku
- VMware Cloud Foundry

### Infrastructure as a Service (IaaS)

**IaaS** provides customers with remote access to back-end infrastructure hosted by a cloud service provider.

Resources can include:

- Data processing servers
- Storage
- Networking resources
- Other infrastructure

Resources are commonly licensed as needed, making IaaS a cost-effective alternative to purchasing and maintaining infrastructure on premises.

## SaaS vs PaaS vs IaaS

| Service | Primary Purpose | Customer Uses |
|---|---|---|
| **SaaS** | Provides ready-to-use applications | Uses applications through a web browser |
| **PaaS** | Provides application development platforms | Builds, manages, and deploys applications |
| **IaaS** | Provides computing infrastructure | Uses servers, storage, networking, and other infrastructure |

## Cloud Security

**Cloud security** is a subfield of cybersecurity focused on protecting **data, applications, and infrastructure in the cloud**.

Moving applications and infrastructure to the cloud can make operating an online business easier, but it can also make protecting data more complicated.

### Traditional IT vs Cloud Environment

In a traditional environment, an organization may have its entire IT infrastructure **on premises**. The organization's internal security team is responsible for protecting those systems.

In cloud environments, security responsibilities are divided between the **cloud service provider** and the **customer**.

## Shared Responsibility Model

The **shared responsibility model** defines how security responsibilities are divided between cloud service providers and their customers.

Customers are commonly responsible for securing anything directly within their control, including:

- **Identity and access management**
- **Resource configuration**
- **Data handling**

The cloud service provider is generally responsible for securing the underlying infrastructure it operates.

For example, in a PaaS environment:

- The customer is responsible for securing the applications they build.
- The cloud service provider is responsible for maintaining the security of the underlying servers and infrastructure.

> **Note:** The amount of responsibility delegated to the cloud service provider varies depending on whether the organization uses **SaaS, PaaS, or IaaS**.

## Cloud Security Challenges

Cloud environments introduce several security challenges.

### Misconfiguration

**Misconfiguration** is one of the biggest concerns in cloud security.

Customers are responsible for configuring parts of their own security environment. Using default or out-of-the-box configurations may fail to address an organization's specific security objectives.

### Cloud-Native Breaches

Cloud-native breaches are more likely to occur due to **misconfigured services**.

### Access Monitoring

Monitoring access to cloud resources can be difficult depending on:

- The customer
- The cloud service being used
- The level of service provided

### Regulatory Compliance

Organizations may also need to meet specific regulatory requirements when using cloud services.

Examples include:

- **Health Insurance Portability and Accountability Act (HIPAA)**
- **Payment Card Industry Data Security Standard (PCI DSS)**
- **General Data Protection Regulation (GDPR)**

## Cloud Security and Cybersecurity Careers

As more businesses adopt cloud-based services, the need for professionals who understand cloud security continues to grow.

Cloud security is identified as an in-demand cybersecurity skill, creating opportunities for security professionals with knowledge of cloud environments and their associated risks.

## Resources for Further Learning

- [U.K. National Cyber Security Centre (NCSC)](https://www.ncsc.gov.uk/collection/cloud/understanding-cloud-services/cloud-security-shared-responsibility-model) - Guidance for choosing, using, and deploying cloud services securely based on the shared responsibility model.
- [Cloud Security Alliance (CSA)](https://cloudsecurityalliance.org/) - Organization focused on creating secure cloud environments and providing cloud security research and resources.
- [CompTIA Cloud+](https://www.comptia.org/blog/your-next-move-cloud-security-specialist) - Certification program covering foundational skills for cloud security specialists.

## Key Takeaways

- **Cloud computing** provides scalable, on-demand services hosted on shared infrastructure and accessed over the internet.
- Cloud-based services are commonly categorized as **SaaS, PaaS, and IaaS**.
- **SaaS** provides ready-to-use applications, **PaaS** provides application development platforms, and **IaaS** provides infrastructure.
- **Cloud security** focuses on protecting data, applications, and infrastructure in cloud environments.
- The **shared responsibility model** divides security responsibilities between cloud providers and customers.
- Customers are commonly responsible for **identity and access management, resource configuration, and data handling**.
- Major cloud security challenges include **misconfiguration, cloud-native breaches, access monitoring, and regulatory compliance**.
- Understanding cloud services and their security requirements is important for cybersecurity professionals.