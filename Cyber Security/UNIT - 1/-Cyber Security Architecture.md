# Cyber Security Architecture – 15 Mark Answer

## 1. Introduction

**Cyber Security Architecture** is a structured approach to protecting an organization's **systems, networks, applications, and data** from cyber threats. It combines **security technologies, policies, processes, and people** to prevent unauthorized access, data modification, attacks, and service disruption.

The main purpose of cybersecurity is to maintain the **Confidentiality, Integrity, and Availability (CIA)** of information. 

---

## 2. Objectives of Cyber Security Architecture

The major objectives are:

1. **Confidentiality** – Ensures that sensitive information is accessible only to authorized users.
2. **Integrity** – Ensures that information is accurate and cannot be modified without authorization.
3. **Availability** – Ensures that systems, networks, and data are available whenever required.
4. **Authentication** – Verifies the identity of users or systems.
5. **Non-repudiation** – Ensures that the sender or receiver cannot deny participation in a communication.  

---

## 3. Basic Architecture of Cyber Security

A cybersecurity architecture can be understood as a **layered security model**:

```text
                 CYBER SECURITY ARCHITECTURE
                           │
        ┌──────────────────┴──────────────────┐
        │                                     │
   Security Policies                     Security Controls
        │                                     │
   ┌────┴─────┐                    ┌──────────┴──────────┐
   │          │                    │                     │
 People     Processes          Technical Controls   Physical Controls
                                  │
             ┌────────────────────┼────────────────────┐
             │                    │                    │
        Network Security     Application Security   Data Security
             │                    │                    │
       Firewall / IDS       Secure Applications    Encryption
       IPS / NAC            Access Control          Hashing
       Segmentation         Authentication          Backup
             │                    │                    │
             └────────────────────┼────────────────────┘
                                  │
                         Monitoring & Response
                                  │
                       Recovery & Continuity
```

The notes emphasize that network security uses **several layers of protection**, both at the network edge and within the network, with rules and controls determining access to resources. 

---

## 4. Major Layers/Components

### A. Physical Security

Physical security protects the hardware, network infrastructure, and facilities from unauthorized physical access.

**Examples:**

* Biometric systems
* Controlled access to server rooms
* Physical protection of network devices

Physical network security is the basic level of protection against unauthorized personnel gaining control over network resources. 

---

### B. Network Security

Network security protects the **confidentiality, integrity, and availability** of computer networks and transmitted data.

Important network security mechanisms include:

* **Firewalls**
* **Intrusion Prevention Systems (IPS)**
* **Antivirus/anti-malware**
* **Network segmentation**
* **Access control**
* **Sandboxing**
* **Secure communications**

A firewall filters incoming and outgoing traffic according to predefined security rules. IPS monitors network activity, identifies malicious activity, reports it, and attempts to block it. 

---

### C. Application Security

Application security protects software and applications from vulnerabilities and attacks.

It involves:

* Secure application development
* Authentication and authorization
* Input validation
* Protection against malicious requests
* Regular security updates

This layer is important because attackers can exploit weaknesses in applications to gain unauthorized access to data.

---

### D. Data and Information Security

Data security protects information during **storage, processing, and transmission**.

Important techniques include:

* **Encryption**
* **Hashing**
* **Digital signatures**
* **Access control**
* **Data classification**
* **Backup and recovery**

Cryptography converts plaintext into ciphertext using an algorithm and key, helping protect confidentiality, integrity, and authenticity. 

---

### E. Identity and Access Management

Identity and access management ensures that only authorized users can access particular resources.

It involves:

* User identification
* Authentication
* Authorization
* Passwords
* Biometrics
* Security tokens
* Multi-factor authentication (MFA)

The notes describe authentication as verifying that a person or system is who they claim to be. 

---

## 5. Defense in Depth

**Defense in Depth** is an important principle of cybersecurity architecture.

It uses **multiple layers of security**, so that if one security mechanism fails, other mechanisms continue to protect the system.

For example:

```text
Internet
   ↓
Firewall
   ↓
Network Segmentation
   ↓
Authentication / Access Control
   ↓
Antivirus / Endpoint Security
   ↓
Encryption
   ↓
Secure Data
```

The notes specifically identify Defense in Depth as using multiple security layers, including **Antivirus, Firewall, Secure Boot, SmartScreen and BitLocker**. 

---

## 6. Information Assurance Model

The **Information Assurance (IA) model** provides another important view of cybersecurity architecture.

It consists of:

### Five Security Services

1. Confidentiality
2. Integrity
3. Availability
4. Authentication
5. Non-repudiation

### Three Information States

1. **Storage** – Data is saved on a storage medium.
2. **Processing** – Data is being processed.
3. **Transmission** – Data is transferred between systems.

### Security Countermeasures

Security countermeasures are based on:

* **People**
* **Policy & Practice**
* **Technology**

The notes describe these dimensions as protecting information throughout its lifecycle and addressing vulnerabilities through technology, policies, practices, and people. 

---

## 7. Security Technologies Used

Some important technologies used in a cybersecurity architecture are:

| Technology               | Purpose                                 |
| ------------------------ | --------------------------------------- |
| **Firewall**             | Filters network traffic                 |
| **IDS/IPS**              | Detects and prevents malicious activity |
| **Antivirus**            | Detects and handles malware             |
| **Encryption**           | Protects data confidentiality           |
| **Hashing**              | Helps verify data integrity             |
| **VPN**                  | Provides protected communication        |
| **Access Control**       | Restricts unauthorized users            |
| **Network Segmentation** | Separates network traffic/resources     |
| **Authentication/MFA**   | Verifies user identity                  |
| **Backup & Recovery**    | Restores data after failures/attacks    |

---

## 8. Role of Firewall in the Architecture

A **firewall** acts as a security boundary between a private internal network and the Internet. It examines incoming and outgoing traffic and allows, rejects, or drops traffic according to security rules. 

Major types include:

* Packet Filtering Firewall
* Stateful Inspection Firewall
* Application Layer Firewall
* Next Generation Firewall (NGFW)
* Hardware Firewall
* Software Firewall

NGFWs can provide features such as **Deep Packet Inspection, Application Inspection, and SSL/SSH inspection**. 

---

## 9. Benefits of Cyber Security Architecture

1. **Protects sensitive information**
2. **Prevents unauthorized access**
3. **Reduces the impact of malware and cyberattacks**
4. **Maintains data integrity**
5. **Improves system availability**
6. **Provides controlled access to resources**
7. **Supports monitoring and incident response**
8. **Helps maintain business continuity**
9. **Provides multiple layers of protection**
10. **Improves overall security management**

---

## 10. Conclusion

Cyber Security Architecture provides a **systematic and layered method of protecting an organization's digital environment**. It combines physical security, network security, application security, data protection, authentication, access control, security policies, and human practices.

The most important foundation is the **CIA triad—Confidentiality, Integrity, and Availability**, supported by **Authentication and Non-repudiation**. A strong architecture follows the **Defense in Depth** principle so that failure of one security control does not compromise the entire system. 

**👉 Exam tip:** For a 15-mark question, draw the **layered architecture diagram**, explain **CIA + Authentication + Non-repudiation**, and write **Defense in Depth + major security components**. This will make the answer look complete and well-structured.
