# Cyber Security Models – 13 Mark Answer

Cybersecurity models provide a structured framework for protecting information, systems and networks. The PDF explains **three important cybersecurity models**:

1. **CIA Triad**
2. **Star Model**
3. **Parkerian Hexad**



---

## 1. CIA Triad

The **CIA Triad** is the foundation of information security. It consists of **Confidentiality, Integrity and Availability**.

### a) Confidentiality

Confidentiality ensures that sensitive information is accessible **only to authorized users**. It prevents information from being viewed, copied or intercepted by unauthorized people.

**Techniques:**

* Encryption
* Passwords
* Biometric authentication
* Access Control Lists (ACLs)
* Data classification

**Example:** Online banking transactions are encrypted to protect customer account details.

**If confidentiality is broken:** A hacker may steal and leak customers' personal information. 

### b) Integrity

Integrity means maintaining the **accuracy, consistency and trustworthiness** of data. It ensures that data cannot be changed, deleted or corrupted by unauthorized users.

**Techniques:**

* Hash functions
* Checksums
* Digital signatures
* Database transaction controls

**Example:** Medical records can use cryptographic checksums to detect unauthorized modifications.

**If integrity is broken:** An attacker may modify financial records, resulting in incorrect reports and loss of trust. 

### c) Availability

Availability ensures that systems, data and resources are accessible to authorized users **whenever required**.

**Techniques:**

* Backup systems
* Redundant systems
* Failover mechanisms
* Load balancing
* DDoS protection

**Example:** Cloud providers replicate data across multiple data centers to maintain continuous access.

**If availability is broken:** A ransomware attack may lock files and prevent legitimate users from accessing them. 

### CIA Triad Summary

**Confidentiality → Keep information secret**
**Integrity → Keep information correct**
**Availability → Keep systems and information accessible** 

---

# 2. Star Model

The **Star Model** extends the CIA Triad by adding **Accountability and Auditability**. It is particularly useful in regulated areas such as **healthcare, banking and government services**. 

It contains:

### a) Confidentiality

Protects sensitive information from unauthorized disclosure.

### b) Integrity

Ensures that information remains accurate and is not improperly modified.

### c) Availability

Ensures that authorized users can access systems and resources when required.

### d) Accountability

Accountability ensures that **users are responsible for their actions** in a system. It also helps prevent users from denying actions they performed.

**Techniques:**

* Secure login credentials
* Activity logs
* User session tracking

**Example:** A banking system records the time, location and user ID for every transaction. 

### e) Auditability

Auditability allows system activities and transactions to be **reviewed and verified**. It supports investigations and compliance checking.

**Techniques:**

* System logging
* Audit trails
* Periodic inspections

**Example:** In healthcare, access to patient records can be logged for compliance purposes. 

---

# 3. Parkerian Hexad

The **Parkerian Hexad**, proposed by **Donn B. Parker**, extends the CIA Triad into **six security elements**. These are:

1. Confidentiality
2. Integrity
3. Availability
4. Possession/Control
5. Authenticity
6. Utility 

### a) Confidentiality

Ensures that information is available only to authorized users.

### b) Integrity

Ensures that information remains accurate and is not improperly changed.

### c) Availability

Ensures that information and systems are accessible when required.

### d) Possession or Control

Possession refers to the **physical control or ownership of information**.

**Example:** If an encrypted company laptop is stolen, confidentiality may still be protected, but possession of the device and information is lost.

**Protection methods:**

* Physical security controls
* Secure storage
* Encrypted portable devices 

### e) Authenticity

Authenticity ensures that **data, messages and identities are genuine** and originate from a trusted source. It helps prevent impersonation and forgery.

**Techniques:**

* Digital signatures
* Digital certificates
* Multi-factor authentication

**Example:** Email authentication protocols such as SPF and DKIM help verify legitimate email sources. 

### f) Utility

Utility means that information is in a **usable, functional and meaningful form** for its intended purpose.

**Example:** A database backup may be available, but if it is stored in an unreadable format, its utility is lost.

**Protection methods:**

* Proper file formats
* Compatible systems
* Data standardization 

---

## Comparison of Cybersecurity Models

| Model               | Main Elements                                     |
| ------------------- | ------------------------------------------------- |
| **CIA Triad**       | Confidentiality, Integrity, Availability          |
| **Star Model**      | CIA + Accountability + Auditability               |
| **Parkerian Hexad** | CIA + Possession/Control + Authenticity + Utility |

### Conclusion

The **CIA Triad** provides the basic foundation of cybersecurity. The **Star Model** extends it by emphasizing accountability and auditability, while the **Parkerian Hexad** provides a broader view by including possession, authenticity and utility. These models help organizations identify security requirements and protect their information and systems effectively.
