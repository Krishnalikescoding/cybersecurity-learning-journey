# Wireless Security Protocols

## Wireless Communication

Wireless communication allows devices to exchange data using **radio waves** instead of physical cables.

**Wi-Fi** is based on the **IEEE 802.11** family of wireless networking standards maintained by the **Institute of Electrical and Electronics Engineers (IEEE)**.

---

# Evolution of Wi-Fi Security

## 1. WEP (Wired Equivalent Privacy)

### Overview
- Introduced in **1999**
- First wireless security protocol
- Designed to provide wired-like security for Wi-Fi

### Limitations
- Weak encryption
- Easily cracked by attackers
- Considered **obsolete and insecure**

---

## 2. WPA (Wi-Fi Protected Access)

### Overview
- Released in **2003**
- Created to replace WEP
- Intended as a temporary improvement while supporting older hardware

### Improvements
- Uses **TKIP (Temporal Key Integrity Protocol)**
- Larger encryption keys
- Includes **Message Integrity Check (MIC)** to detect altered packets

### Vulnerability
- Susceptible to **KRACK (Key Reinstallation Attack)**, allowing attackers to manipulate the authentication process and potentially decrypt traffic.

---

## 3. WPA2

### Overview
- Released in **2004**
- Became the standard for Wi-Fi security

### Improvements
- Uses **AES (Advanced Encryption Standard)** for stronger encryption
- Uses **CCMP (Counter Mode Cipher Block Chaining Message Authentication Code Protocol)** for encryption, authentication, and integrity
- More secure than WPA

### Limitation
- Still vulnerable to **KRACK attacks**

---

### WPA2 Modes

#### Personal
- Best for **home networks**
- Uses a shared password (pre-shared key)
- Easy to configure

#### Enterprise
- Designed for **businesses and organizations**
- Individual user authentication
- Centralized access management
- Users do not know the network encryption keys

---

## 4. WPA3

### Overview
- Released in **2018**
- Current and most secure Wi-Fi protocol

### Improvements
- Protects against **KRACK attacks**
- Uses **SAE (Simultaneous Authentication of Equals)** for stronger authentication
- Prevents offline password-guessing attacks
- Uses **128-bit encryption**
- **WPA3-Enterprise** supports optional **192-bit encryption**

---

# Wireless Security Comparison

| Protocol | Year | Encryption | Status | Main Weakness |
|----------|------|------------|--------|---------------|
| **WEP** | 1999 | Weak encryption | Obsolete | Easily cracked |
| **WPA** | 2003 | TKIP | Legacy | Vulnerable to KRACK |
| **WPA2** | 2004 | AES + CCMP | Current standard | Vulnerable to KRACK |
| **WPA3** | 2018 | SAE + AES | Most Secure | Addresses KRACK vulnerabilities |

---

# Important Technologies

| Technology | Purpose |
|------------|---------|
| **TKIP** | Improved encryption used in WPA |
| **AES** | Strong encryption algorithm used in WPA2 and WPA3 |
| **CCMP** | Provides encryption, authentication, and message integrity in WPA2 |
| **SAE** | Secure authentication method used in WPA3 |

---

# Importance for Security Analysts

Security analysts should:

- Identify outdated Wi-Fi security protocols.
- Replace **WEP** and **WPA** with modern alternatives.
- Prefer **WPA3** whenever supported.
- Use **WPA2-Enterprise** or **WPA3-Enterprise** in organizational environments.
- Regularly update wireless devices to reduce security risks.

---

# Key Takeaways

- **Wi-Fi** is based on the **IEEE 802.11** wireless networking standards.
- **WEP (1999)** was the first Wi-Fi security protocol but is now obsolete because of weak encryption.
- **WPA (2003)** improved security with **TKIP** and **Message Integrity Check (MIC)** but remained vulnerable to **KRACK attacks**.
- **WPA2 (2004)** became the Wi-Fi security standard by introducing **AES** encryption and **CCMP**, although it can still be affected by KRACK.
- **WPA3 (2018)** is the most secure wireless protocol, using **SAE** authentication, stronger encryption, and protection against KRACK and offline password attacks.
- Organizations should use **WPA2-Enterprise** or **WPA3-Enterprise** to provide centralized authentication and stronger wireless security.