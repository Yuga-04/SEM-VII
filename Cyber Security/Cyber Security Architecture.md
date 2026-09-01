# Security Principles – 15 Mark Answer

## 1. Introduction

**Security principles** are fundamental rules used to design and operate secure computer systems. They help protect **users, devices, applications, networks, and data** from unauthorized access, modification, malware, and other security threats.

The major security principles covered in the notes include **Principle of Least Privilege, User Account Control, Secure by Default, Defense in Depth, Identity and Access Management, and Patch Management**. 

---

## 2. Principle of Least Privilege (PoLP)

The **Principle of Least Privilege** states that users and processes should have **only the permissions necessary to perform their required tasks and nothing more**.

### Purpose:

* Reduces unauthorized access.
* Limits the damage caused by malware.
* Prevents accidental changes by users.
* Reduces the impact if an account is compromised.

### Example:

A normal user cannot install software unless **administrator permission** is provided. 

---

## 3. User Account Control (UAC)

**User Account Control (UAC)** ensures that applications normally operate with **standard user privileges** unless administrator permission is explicitly granted.

### Purpose:

* Prevents unauthorized system changes.
* Stops applications from automatically obtaining administrator privileges.
* Alerts the user when an application requires elevated permissions.

### Example:

When a program tries to install software or make important system changes, Windows displays a permission prompt. 

---

## 4. Secure by Default

**Secure by Default** means that system components and services should be configured in their **most secure state by default**.

### Purpose:

* Reduces security gaps.
* Prevents insecure configurations.
* Provides protection even when users do not manually configure security settings.

### Example:

Windows Firewall can be enabled automatically, providing basic network protection. 

---

## 5. Defense in Depth

**Defense in Depth** means using **multiple layers of security** so that if one security mechanism fails, other mechanisms can still protect the system.

### Security layers include:

* Antivirus
* Firewall
* Secure Boot
* SmartScreen
* BitLocker
* User Account Control

### Example:

```text
              ATTACKER
                  ↓
              FIREWALL
                  ↓
          NETWORK SECURITY
                  ↓
          AUTHENTICATION
                  ↓
             ANTIVIRUS
                  ↓
             ENCRYPTION
                  ↓
             SECURE DATA
```

If malware bypasses one layer, other security mechanisms can still block or limit it. 

---

## 6. Identity and Access Management (IAM)

**Identity and Access Management** ensures that users are properly **authenticated and authorized** before accessing resources.

### Technologies:

* Windows Hello
* Active Directory
* Azure AD
* PIN
* Biometrics
* Multi-factor authentication

### Purpose:

It provides secure and flexible methods for verifying users and controlling what resources they can access. 

---

## 7. Authentication

**Authentication** verifies whether a person or system is actually who they claim to be.

Common authentication methods include:

1. Passwords
2. Biometrics
3. Security tokens
4. Multi-factor authentication (MFA)

For example, logging into an account using a **password + OTP** provides stronger authentication than a password alone. 

---

## 8. Patch Management

**Patch Management** involves regularly updating operating systems and software to fix known security vulnerabilities.

### Purpose:

* Fixes security weaknesses.
* Prevents attackers from exploiting known vulnerabilities.
* Improves system security and reliability.

Windows provides regular security updates through **Windows Update**. 

---

## 9. CIA Security Principles

Security architecture is also based on the **CIA Triad**:

### Confidentiality

Ensures that information is accessible only to authorized people.

**Example:** Only authorized doctors can access patient records.

### Integrity

Ensures that data is not modified without authorization.

**Example:** Hashing and digital signatures can help detect data modification.

### Availability

Ensures that systems and data are available when required.

**Example:** A bank's online service should remain available to customers. 

---

## 10. Importance of Security Principles

Security principles are important because they:

* Protect sensitive information.
* Prevent unauthorized access.
* Reduce the impact of malware.
* Protect system integrity.
* Improve availability.
* Control user privileges.
* Reduce security vulnerabilities.
* Provide multiple layers of protection.
* Support secure system design.

---

## Conclusion

Security principles provide the **foundation for designing secure computer systems**. Principles such as **Least Privilege, UAC, Secure by Default, Defense in Depth, Identity and Access Management, Authentication, and Patch Management** work together to protect systems and data.

Among these, **Defense in Depth** is especially important because it ensures that a single security failure does not compromise the entire system. Together with the **CIA Triad—Confidentiality, Integrity, and Availability**, these principles form the basis of effective cybersecurity. 

### ⭐ Easy way to remember

**L – U – S – D – I – P**

**L** → Least Privilege
**U** → User Account Control
**S** → Secure by Default
**D** → Defense in Depth
**I** → Identity & Access Management
**P** → Patch Management
