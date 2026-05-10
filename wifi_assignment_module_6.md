# Wi‑Fi Training Program – Module 6 Assignment

## 1. What are the pillars of Wi‑Fi security?

Wi‑Fi security is built on several important principles that protect wireless communication and ensure that only authorized users can access the network.

### Main Pillars of Wi‑Fi Security

#### Authentication

Authentication verifies the identity of users or devices before granting access to the wireless network.

Examples include:

- WPA2‑Personal using a passphrase
- WPA2/WPA3‑Enterprise using 802.1X authentication

#### Encryption

Encryption protects wireless data by converting it into an unreadable format during transmission.

It prevents attackers from reading intercepted traffic.

Examples include:

- TKIP
- AES‑CCMP
- GCMP

#### Integrity

Integrity mechanisms ensure that transmitted data is not modified during communication.

Message Integrity Check (MIC) mechanisms are used to detect tampering.

#### Access Control

Access control determines which users or devices are allowed to join the network.

Examples include:

- MAC filtering
- 802.1X authentication
- Role-based access policies

#### Availability

Availability ensures that wireless services remain accessible and operational.

Security mechanisms should also protect the network from denial-of-service attacks and excessive interference.

Together, these pillars provide confidentiality, reliability, and controlled access in wireless networks.

---

## 2. Explain the difference between authentication and encryption in Wi‑Fi security.

Authentication and encryption are both important parts of wireless security, but they perform different functions.

### Authentication

Authentication is the process of verifying the identity of a user or device.

Its purpose is to confirm whether a client is allowed to access the wireless network.

Examples:

- WPA2‑PSK passphrase validation
- 802.1X authentication using usernames and certificates

Authentication answers the question:

“Who are you?”

### Encryption

Encryption protects the actual data transmitted over the wireless medium.

The data is converted into ciphertext so unauthorized users cannot read it.

Examples:

- AES encryption
- TKIP encryption

Encryption answers the question:

“Can anyone read the transmitted data?”

### Difference

- Authentication controls network access.
- Encryption protects data confidentiality.

Both are required for secure wireless communication.

---

## 3. Explain the differences between WEP, WPA, WPA2, and WPA3.

Wireless security standards evolved over time to improve security and overcome weaknesses in earlier protocols.

### WEP – Wired Equivalent Privacy

WEP was the first security protocol used in Wi‑Fi networks.

#### Characteristics

- Used RC4 encryption
- Static key-based security
- Weak initialization vector design
- Vulnerable to attacks

WEP is now considered highly insecure.

### WPA – Wi‑Fi Protected Access

WPA was introduced as an improvement over WEP.

#### Characteristics

- Introduced TKIP encryption
- Dynamic key generation
- Better integrity protection
- Temporary replacement for WEP

Although WPA improved security, TKIP still had limitations.

### WPA2

WPA2 became the standard replacement for WPA.

#### Characteristics

- Uses AES‑CCMP encryption
- Stronger encryption and integrity mechanisms
- Supports Personal and Enterprise modes
- Much more secure than WEP and WPA

WPA2 became the most widely used wireless security standard.

### WPA3

WPA3 is the latest Wi‑Fi security standard.

#### Characteristics

- Improved authentication security
- Protection against offline dictionary attacks
- Stronger encryption methods
- Forward secrecy support
- Better security for open networks

### Overall Evolution

- WEP: weak and insecure
- WPA: temporary improvement
- WPA2: strong modern security
- WPA3: enhanced next-generation wireless security

---

## 4. Why is WEP considered insecure compared to WPA2 or WPA3?

WEP is considered insecure because of major weaknesses in its encryption and key management design.

### Reasons WEP is Insecure

#### Weak Initialization Vectors

WEP uses short initialization vectors that repeat frequently, making it easier for attackers to analyze traffic.

#### Static Encryption Keys

The same key is often reused for long periods, increasing vulnerability.

#### RC4 Weaknesses

WEP uses RC4 encryption in an insecure implementation that allows key recovery attacks.

#### Weak Integrity Protection

The integrity mechanism in WEP is not secure against packet modification attacks.

#### Easy Key Cracking

Attackers can capture packets and recover WEP keys within a short time using publicly available tools.

### Why WPA2 and WPA3 are More Secure

- Use stronger encryption methods such as AES
- Support dynamic key generation
- Provide stronger authentication
- Include better integrity protection
- Resist known cryptographic attacks more effectively

Because of these weaknesses, WEP is obsolete and should not be used in modern networks.

---

## 5. Why was WPA2 introduced?

WPA2 was introduced to replace WPA and provide stronger wireless security.

### Reasons for Introducing WPA2

#### Stronger Encryption

WPA2 introduced AES‑CCMP encryption, which is much more secure than TKIP used in WPA.

#### Better Integrity Protection

Improved mechanisms were added to protect against packet tampering.

#### Improved Authentication

WPA2 supports stronger enterprise authentication methods using 802.1X.

#### Long-Term Security

WPA was intended as a temporary solution. WPA2 was designed as a more secure and standardized long-term replacement.

### Importance of WPA2

WPA2 became the standard wireless security protocol for enterprise and home networks because of its stronger cryptographic protection.

---

## 6. What is the role of the Pairwise Master Key (PMK) in the 4-way handshake?

The Pairwise Master Key (PMK) is the primary key used during the WPA/WPA2/WPA3 4-way handshake process.

### Role of PMK

- Acts as the root key for deriving session keys
- Confirms that both the client and access point possess the same secret
- Used to generate the Pairwise Transient Key (PTK)

### PMK Generation

- In WPA/WPA2‑Personal, the PMK is derived from the passphrase.
- In Enterprise mode, the PMK is generated during 802.1X authentication.

### Importance

The PMK itself is not directly used for encrypting user traffic.

Instead, it is used to derive temporary encryption keys securely during the handshake process.

Without a valid PMK, the 4-way handshake cannot complete successfully.

---

## 7. How does the 4-way handshake ensure mutual authentication between the client and the access point?

The 4-way handshake confirms that both the client and access point possess the same PMK without directly transmitting the PMK itself.

### Authentication Process

#### Step 1

The access point sends a random nonce value called ANonce to the client.

#### Step 2

The client generates its own nonce called SNonce.

Using the PMK, ANonce, SNonce, and MAC addresses, the client derives the PTK and sends a Message Integrity Code (MIC) to the AP.

#### Step 3

The AP independently derives the same PTK and verifies the MIC.

If the MIC is correct, the AP confirms that the client possesses the correct PMK.

The AP then sends the GTK and installation information.

#### Step 4

The client verifies the AP message and confirms successful key installation.

### Mutual Authentication

- The client proves knowledge of the PMK to the AP.
- The AP proves knowledge of the PMK to the client.

This process establishes trust between both devices before encrypted communication begins.

---

## 8. What will happen if we put a wrong passphrase during a 4-way handshake?

If the client uses an incorrect passphrase, the PMK generated by the client will differ from the PMK generated by the access point.

### What Happens During the Handshake

- The client derives an incorrect PTK.
- The Message Integrity Code (MIC) generated by the client will not match the AP calculation.
- The AP fails to validate the handshake messages.

### Result

- The 4-way handshake fails.
- Encryption keys are not installed.
- The client cannot complete authentication.
- The wireless connection is rejected.

### User Impact

The user typically sees messages such as:

- “Incorrect password”
- “Authentication failed”
- “Unable to connect to network”

The failure occurs because both sides cannot derive matching encryption keys.

---

## 9. What problem does 802.1X solve in a network?

802.1X is a network access control framework used for authentication in wired and wireless networks.

### Problem Solved by 802.1X

Without proper authentication, unauthorized users could gain access to network resources.

802.1X solves this problem by ensuring that users and devices are authenticated before network access is granted.

### Functions of 802.1X

- Centralized authentication
- User identity verification
- Dynamic key generation
- Controlled network access
- Improved enterprise security

### Components

- Supplicant: the client device
- Authenticator: the AP or switch
- Authentication Server: usually a RADIUS server

### Importance

802.1X is widely used in enterprise environments because it provides scalable and secure network authentication.

---

## 10. How does 802.1X enhance security over wireless networks?

802.1X enhances wireless security by providing strong authentication and dynamic security mechanisms.

### Security Enhancements Provided by 802.1X

#### Strong User Authentication

Users are authenticated using credentials, certificates, or enterprise identity systems.

#### Dynamic Key Generation

Encryption keys are generated dynamically for each session instead of using static shared keys.

#### Centralized Authentication

Authentication is handled using centralized servers such as RADIUS.

#### Improved Access Control

Only authenticated users are allowed network access.

#### Better Security Management

Policies and user permissions can be controlled centrally.

### Advantages Over Pre-Shared Keys

- Better scalability
- Improved accountability
- Stronger authentication
- Reduced risk of password sharing
- Better enterprise security

802.1X is a critical security framework for modern enterprise wireless networks.

