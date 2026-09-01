# Principle of Least Privilege

## Overview

The **Principle of Least Privilege (PoLP)**, also referred to as **least privilege**, is a fundamental security control used to protect sensitive data and resources.

**Principle of Least Privilege:** A security concept in which a user is granted only the minimum level of access and authorization required to complete a task or function.

Least privilege supports the **Confidentiality, Integrity, and Availability (CIA) triad** by reducing unnecessary access to systems and information.

## How Least Privilege Reduces Risk

Organizations need to account for risks such as data theft, misuse, and abuse.

Implementing least privilege can reduce the risk of costly security incidents by:

- Limiting access to sensitive information.
- Reducing accidental data modification, tampering, or loss.
- Supporting system monitoring and administration.
- Reducing the likelihood of successful attacks by limiting what specific users can access and do.

Least privilege should be applied to organizational assets by clearly defining **who or what the users are** and determining the access they require.

### Separation of Duties

Least privilege is closely related to **separation of duties**.

**Separation of Duties:** A security concept that divides tasks and responsibilities among different users to prevent a single user from having complete control over critical business functions.

## Determining Access and Authorization

Before implementing least privilege, organizations need to determine:

1. **Who is the user?**
2. **How much access does the user need to a specific resource?**

### Identifying Users

A user can be:

- A person, such as a customer, employee, or vendor.
- A device connected to the organization's network.
- Software that interacts with other software on the network.

In general, each user should have their own account.

User accounts are typically stored and managed through an organization's **directory service**.

## Types of User Accounts

| Account Type | Description |
|---|---|
| **Guest Account** | Provided to external users who need access to an internal network, such as customers, clients, contractors, or business partners. |
| **User Account** | Assigned to staff based on their job duties. |
| **Service Account** | Granted to applications or software that needs to interact with other software on the network. |
| **Privileged Account** | Has elevated permissions or administrative access. |

Organizations should establish a **baseline access level** for each account type before implementing least privilege.

However, access requirements can change depending on the user's current task or situation.

### Example: Customer Support

A customer support representative may need temporary access to customer information while assisting with a reservation.

Once the representative begins working with another customer, the previous customer's information should no longer be accessible to them.

This demonstrates why user accounts must be **routinely and consistently monitored**.

> **Pro Tip:** Passwords are also important when implementing least privilege. Even when accounts have appropriate permissions, an insecure password can compromise systems.

## Auditing Account Privileges

Configuring appropriate user accounts and assigning the correct privileges is an important first step. However, accounts must also be **periodically audited** to maintain security.

Three common approaches to auditing user accounts are:

1. **Usage audits**
2. **Privilege audits**
3. **Account change audits**

## Usage Audits

**Usage audits** review:

- Which resources each account is accessing.
- What users are doing with those resources.

Usage audits can help determine:

- Whether users are following organizational security policies.
- Whether users have permissions that are no longer needed and can be revoked.

## Privilege Audits

Users can accumulate more access privileges than they need over time. This is known as **privilege creep**.

**Privilege Creep:** The accumulation of unnecessary access privileges over time.

Privilege creep can occur when:

- An employee is promoted.
- An employee changes teams.
- An employee's job duties change.

**Privilege audits** assess whether a user's role is aligned with the resources they can access.

## Account Change Audits

Directory services maintain records and logs associated with user accounts.

Account changes are typically recorded and can be reviewed for suspicious activity.

For example:

- Multiple attempts to change an account password may indicate suspicious activity.

**Account change audits** help ensure that changes to user accounts are made only by authorized users.

> **Note:** Most directory services can be configured to alert system administrators about suspicious activity.

## Key Takeaways

- **Least privilege** grants users only the minimum access and authorization required to perform their tasks.
- Least privilege supports the **CIA triad** and reduces the risk of unauthorized access.
- Users should have clearly defined accounts and appropriate access levels.
- Common account types include **guest, user, service, and privileged accounts**.
- Access requirements can change depending on a user's current role or task.
- User accounts should be routinely monitored and audited.
- **Usage audits** examine how accounts access and use resources.
- **Privilege audits** identify unnecessary permissions and help detect **privilege creep**.
- **Account change audits** review changes to user accounts for suspicious or unauthorized activity.
- Removing unnecessary access rights helps maintain the **confidentiality, integrity, and availability** of information.