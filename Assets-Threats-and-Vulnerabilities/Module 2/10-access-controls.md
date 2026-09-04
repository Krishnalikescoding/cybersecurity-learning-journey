# Access Controls

Protecting data is a fundamental feature of **security controls**. While **hashing** and **encryption** are powerful tools for protecting information, they have limitations. Managing **who or what has access** to information is also essential for keeping data safe and secure.

**Access Controls:** Security controls that manage **access, authorization, and accountability** of information.

When implemented effectively, access controls help maintain:

- **Confidentiality** of data
- **Integrity** of data
- **Availability** of data
- **Efficient access** to information for authorized users

Access controls are commonly divided into three related functions known as the **Authentication, Authorization, and Accounting (AAA) framework**.

Each function has its own protocols and systems that allow it to operate.

## Authentication

**Authentication:** An access control process used to verify **who a user is** before allowing them to access information or a system.

Authentication essentially asks:

> **"Who are you?"**

Organizations determine how they authenticate users based on the objectives of their **security policies**. Authentication can be based on three main factors.

### Three Factors of Authentication

| Factor | What it means | Examples |
|---|---|---|
| **Knowledge** | Something the user **knows** | Password, security question |
| **Ownership** | Something the user **possesses** | One-time passcode (OTP) |
| **Characteristic** | Something the user **is** | Fingerprint, facial scan |

### 1. Knowledge

**Authentication by knowledge:** Authentication based on something the user knows.

Examples include:

- **Password**
- **Security question** and its answer

For example, a website may ask a user to enter a password that was previously created.

### 2. Ownership

**Authentication by ownership:** Authentication based on something the user possesses.

A commonly used example is a **One-Time Passcode (OTP)**.

**One-Time Passcode (OTP):** A randomly generated number sequence sent to a user through a method such as text message or email, which the user must provide to verify their identity.

For example:

1. A user attempts to log in.
2. The application generates a random OTP.
3. The OTP is sent to the user's phone or email.
4. The user enters the OTP.
5. The system verifies the code.

### 3. Characteristic

**Authentication by characteristic:** Authentication based on something the user physically is or a unique characteristic of the user.

This is commonly known as **biometric authentication**.

Examples include:

- **Fingerprint scans**
- **Facial scans**

Biometric authentication is becoming more common because it can be more difficult for criminals to impersonate someone when authentication requires characteristics such as a fingerprint or facial scan rather than only a password.

## Authentication Process

For authentication to work, the information provided by the user must match the information stored by the access control system.

The process can be summarized as:

1. The user provides authentication credentials.
2. The system compares the provided information with the information on file.
3. If the credentials **match**, authentication succeeds and access is **granted**.
4. If the credentials **do not match**, authentication fails and access is **denied**.

| Authentication Result | Outcome |
|---|---|
| Credentials match | **Access granted** |
| Credentials do not match | **Access denied** |

Incorrectly denying access to an authorized user can be frustrating. However, incorrectly granting access to an unauthorized user can create a much more serious security problem.

## Single Sign-On (SSO)

**Single Sign-On (SSO):** A technology that combines several different logins into a single authentication process.

Without SSO, users may need to authenticate separately every time they access a different company resource.

With SSO:

1. The user authenticates **once**.
2. SSO establishes the user's identity.
3. The user can access multiple authorized company resources without repeatedly authenticating.
4. This makes access faster and more convenient.

### Benefits of SSO

- Reduces the number of times users need to log in.
- Speeds up the authentication process.
- Makes access to company resources more convenient.
- Allows users to authenticate once and access multiple resources.

### SSO Security Limitation

Although SSO improves convenience, using SSO **alone** can introduce a significant vulnerability.

If an SSO system relies on only **one authentication factor**, compromising that single factor can potentially allow an attacker to gain access to multiple resources.

Therefore:

> **SSO improves convenience, but it should not rely on only a single authentication factor.**

## Multi-Factor Authentication (MFA)

**Multi-Factor Authentication (MFA):** A security measure that requires a user to verify their identity using **two or more independent authentication factors** before accessing a system or network.

MFA combines multiple types of credentials to provide stronger authentication.

For example:

- **Knowledge + Ownership**
  - Password + One-Time Passcode
- **Knowledge + Characteristic**
  - Password + Fingerprint
- **Ownership + Characteristic**
  - Security token + Fingerprint

The key idea is that the factors should be **independent**. Compromising one factor should not automatically compromise the others.

## SSO vs MFA

SSO and MFA serve different purposes and can be used together.

| SSO | MFA |
|---|---|
| Combines multiple logins into one authentication process | Requires two or more authentication factors |
| Primarily improves **convenience** | Primarily improves **security** |
| Allows users to authenticate once and access multiple resources | Requires users to verify their identity in multiple ways |
| Can be vulnerable when used with only one authentication factor | Strengthens authentication by adding additional factors |

### Using SSO and MFA Together

**SSO and MFA are often used together** to provide both convenience and security.

- **SSO** reduces repeated authentication and makes access faster.
- **MFA** adds additional authentication factors to strengthen security.
- Together, they provide **convenient and secure access** to organizational resources.

## Key Takeaways

- **Access controls** manage access, authorization, and accountability of information.
- Access controls help maintain **confidentiality, integrity, and availability**.
- The three main authentication factors are:
  1. **Knowledge**: something you know.
  2. **Ownership**: something you possess.
  3. **Characteristic**: something you are.
- **Authentication** verifies a user's identity before granting access.
- **SSO** combines several logins into one authentication process.
- **MFA** requires two or more independent authentication factors.
- Using **SSO and MFA together** can provide both convenience and stronger security.