# Encryption

## Previously Learned Terms

* **Encryption:** The process of converting data from a readable format to an encoded format.
* **Public Key Infrastructure (PKI):** An encryption framework that secures the exchange of online information.
* **Cipher:** An algorithm that encrypts information.

Encryption helps keep digital information **private, safe, and secure**. It transforms information into a form that unintended recipients cannot understand.

This section covers:

* **Symmetric encryption**
* **Asymmetric encryption**
* **Key length**
* Common encryption algorithms
* Key generation
* **Kerckhoffs's principle**
* Practical uses of encryption
* Encryption compliance regulations

---

## Types of Encryption

There are two main types of encryption:

### Symmetric Encryption

**Symmetric encryption:** The use of a **single secret key** to exchange information.

* The same key is used for both **encryption and decryption**.
* The sender and receiver must both know the secret key.
* The key is used to lock and unlock the cipher.

### Asymmetric Encryption

**Asymmetric encryption:** The use of a **public and private key pair** for encryption and decryption of data.

* It uses two separate keys:

  * **Public key:** Used to encrypt data.
  * **Private key:** Used to decrypt data.
* The private key is only given to users with authorized access.

### Symmetric vs Asymmetric Encryption

| Feature        | Symmetric Encryption              | Asymmetric Encryption                                |
| -------------- | --------------------------------- | ---------------------------------------------------- |
| Number of keys | One secret key                    | Public and private key pair                          |
| Encryption     | Secret key                        | Public key                                           |
| Decryption     | Secret key                        | Private key                                          |
| Main advantage | Faster processing                 | Allows secure key exchange                           |
| Common use     | Encrypting larger amounts of data | Protecting sensitive data and exchanging information |

---

## The Importance of Key Length

Ciphers are vulnerable to **brute-force attacks**, which use a trial-and-error process to discover private information.

A brute-force attack is similar to trying every possible combination on a combination lock until the correct one is found.

### Key Length and Security

* In modern encryption, **longer key lengths are generally more secure**.
* Longer keys create more possible combinations for an attacker to try.
* This makes brute-force attacks more difficult.

### Key Length and Performance

Longer encryption keys have a drawback:

* They require **more processing time**.
* Shorter keys are generally **less secure**, but they can be faster to compute.

Therefore, encryption involves balancing:

> **Security ↔ Performance**

The goal is to provide fast data communication while keeping information secure.

---

# Approved Algorithms

Many web applications use a **combination of symmetric and asymmetric encryption**.

This allows applications to balance:

* **Security**
* **Performance**
* **User experience**

Security analysts should be familiar with widely used encryption algorithms.

---

## Symmetric Algorithms

### Triple DES (3DES)

**Triple DES (3DES):** A symmetric block cipher that applies the DES algorithm three times using three different 56-bit keys.

* 3DES is known as a **block cipher** because it converts plaintext into ciphertext in blocks.
* It originated from the **Data Encryption Standard (DES)**.
* DES was developed in the **early 1970s**.
* DES generated **64-bit keys**, although only **56 bits** were used for encryption.
* A **bit** is the smallest unit of data measurement on a computer.
* Triple DES applies the DES algorithm **three times** using three different 56-bit keys.
* This results in an **effective key length of 168 bits**.
* Many organizations are moving away from 3DES because of limitations on the amount of data that can be encrypted.
* 3DES is likely to remain in use in some situations for **backwards compatibility**.

### Advanced Encryption Standard (AES)

**Advanced Encryption Standard (AES):** A symmetric encryption algorithm that generates 128-bit, 192-bit, or 256-bit keys.

* AES is considered one of the most secure symmetric algorithms.
* AES supports key lengths of:

  * **128 bits**
  * **192 bits**
  * **256 bits**
* These key sizes are considered safe from brute-force attacks.
* It is estimated that brute-forcing an AES 128-bit key could take a modern computer **billions of years**.

---

## Asymmetric Algorithms

### Rivest Shamir Adleman (RSA)

**Rivest Shamir Adleman (RSA):** An asymmetric encryption algorithm that produces a public and private key pair.

* RSA is named after its three creators.
* It was developed while they were at the **Massachusetts Institute of Technology (MIT)**.
* RSA was one of the first asymmetric encryption algorithms.
* It produces:

  * A **public key**
  * A **private key**
* Asymmetric algorithms such as RSA generally use longer key lengths because they create two keys.
* RSA key sizes include:

  * **1,024 bits**
  * **2,048 bits**
  * **4,096 bits**
* RSA is mainly used to protect **highly sensitive data**.

### Digital Signature Algorithm (DSA)

**Digital Signature Algorithm (DSA):** A standard asymmetric algorithm introduced by NIST in the early 1990s.

* DSA generates **2,048-bit keys**.
* It is widely used as a complement to **RSA** in **Public Key Infrastructure (PKI)**.

---

# Generating Keys

Organizations must implement encryption algorithms when choosing an algorithm to protect their data.

### OpenSSL

**OpenSSL:** An open-source command-line tool that can be used to generate public and private keys.

OpenSSL is commonly used by computers to:

* Generate **public keys**
* Generate **private keys**
* Verify **digital certificates**
* Support processes involved in **Public Key Infrastructure (PKI)**

> **Note:** OpenSSL is only one option. Various other tools are available that can generate keys using common encryption algorithms.

### Heartbleed Bug

In early **2014**, OpenSSL disclosed a vulnerability known as the [**Heartbleed bug**](https://en.wikipedia.org/wiki/Heartbleed).

The vulnerability:

* Exposed sensitive data stored in the memory of websites and applications.
* Affected unpatched versions of OpenSSL.
* Was patched later in **2014**.

Many businesses continue to use secure versions of OpenSSL to generate public and private keys.

**Key lesson:** Using **up-to-date software** is important for maintaining security.

---

# Obscurity Is Not Security

In cryptography, a cipher must be proven to be secure rather than relying on secrecy about how it works.

## Kerckhoffs's Principle

[**Kerckhoffs's principle:**](https://en.wikipedia.org/wiki/Kerckhoffs%27s_principle) A cryptographic system should be designed so that all details of the algorithm, except the private key, can be publicly known without compromising its security.

For example:

* The details of how **AES** works can be publicly available.
* AES can still remain secure.
* The security of the system should depend on keeping the **private key** secret, not the algorithm itself.

### Custom Encryption Algorithms

Some organizations create their own custom encryption algorithms.

However:

* Secret cryptographic systems have sometimes been quickly cracked after being made public.
* Keeping the algorithm itself secret does not guarantee security.

> **Pro Tip:** A cryptographic system should **not** be considered secure if it requires secrecy about how it works.

---

# Encryption Is Everywhere

Companies use both **symmetric and asymmetric encryption**. The two methods often work together to balance security and user experience.

### Example: Web Sessions

Websites may use asymmetric encryption to secure small amounts of important data.

For example:

1. **Login information** such as usernames and passwords may be secured using asymmetric encryption during login requests.
2. After the user gains access, the rest of the web session may switch to **symmetric encryption**.
3. Symmetric encryption is useful for the rest of the session because of its **faster processing speed**.

This approach combines:

* The security benefits of **asymmetric encryption**
* The speed of **symmetric encryption**

---

# Encryption and Compliance

Data encryption is increasingly required by law and regulations.

Two examples include:

* **Federal Information Processing Standards (FIPS 140-3)**
* **General Data Protection Regulation (GDPR)**

These regulations outline how data should be:

* Collected
* Used
* Handled

Achieving compliance with these regulations is important for demonstrating to:

* **Business partners**
* **Governments**

that customer data is handled responsibly.

---

# Key Takeaways

* **Symmetric encryption** relies on a single secret key to protect data.
* **Asymmetric encryption** uses a public and private key pair.
* Longer encryption keys generally provide greater resistance to **brute-force attacks**, but can require more processing time.
* **3DES** is a symmetric block cipher that applies DES three times.
* **AES** is a widely used symmetric encryption algorithm with 128-bit, 192-bit, and 256-bit key sizes.
* **RSA** is an asymmetric encryption algorithm that uses public and private keys.
* **DSA** is an asymmetric algorithm commonly used as a complement to RSA in PKI.
* **OpenSSL** can be used to generate public and private keys and verify digital certificates.
* The **Heartbleed bug** demonstrated the importance of keeping software up to date.
* **Kerckhoffs's principle** states that the security of a cryptographic system should not depend on keeping the algorithm secret.
* Symmetric and asymmetric encryption are often used together to balance **security and performance**.
* Encryption helps organizations protect data and meet **compliance requirements** such as FIPS 140-3 and GDPR.
