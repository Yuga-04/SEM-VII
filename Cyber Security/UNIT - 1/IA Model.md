# Architecture of Cyber Security – 13 Marks

According to the given **Unit-1 PDF**, the cybersecurity architecture can be understood through the **Information Assurance (IA) model**. It provides a structured way to protect information during its different states and against different security risks. The model combines **information states, security services, security countermeasures, and time**. 

## 1. Information States

Information exists in **three different states**:

### a) Transmission

Transmission refers to the time when data is **moving between processing steps or systems**.

**Example:** When a user sends an email to another person, the information travels through a network during delivery.

### b) Storage

Storage refers to the period during which information is **saved on a storage medium**.

**Example:** Saving a document on the disk of a file server.

### c) Processing

Processing refers to the state in which data is **being processed by a system**.

**Example:** Data being processed in the **RAM of a workstation**. 

---

## 2. Security Services

Security services form a **fundamental part of the cybersecurity architecture**. The PDF identifies five important services. 

### a) Confidentiality

Confidentiality ensures that information is **not disclosed to unauthorized people**. Only authorized users should be able to access and understand sensitive information.

It protects against both malicious access and accidental disclosure. 

**Example:** Only authorized employees can access confidential company information.

### b) Integrity

Integrity ensures that information remains **accurate and trustworthy**. Data should not be created, changed, or deleted without proper authorization. 

**Example:** An attacker should not be able to modify a student's examination marks without authorization.

### c) Availability

Availability ensures **reliable and continuous access** to information for authorized users. It also includes measures to maintain access even when there are system failures or interference. 

**Example:** An online banking service should remain available to customers when required.

### d) Authentication

Authentication verifies the **identity of an individual** before allowing access to information or services. 

**Example:** Logging into an account using a username and password.

### e) Non-Repudiation

Non-repudiation ensures that the **sender or receiver cannot later deny their participation in a data transmission**. It can provide evidence about the sender and delivery of information. 

**Example:** A digitally signed document can provide proof that a particular person sent or signed it.

---

## 3. Security Countermeasures

Security countermeasures are used to protect systems from **immediate vulnerabilities and threats**. The PDF identifies three major areas: **People, Policy & Practice, and Technology**. 

### a) People

People are an important part of information security. Administrators and users must understand security policies and practices and should be trained to act appropriately to safeguard the system. 

**Example:** Training employees to identify phishing emails.

### b) Policy and Practice

Organizations establish **security policies and rules** that employees must follow. These policies help in properly handling sensitive information, especially when a system is compromised. 

**Example:** A company may have a policy requiring strong passwords and controlled access to confidential files.

### c) Technology

Technology provides technical protection against vulnerabilities and threats.

Examples include:

* Firewalls
* Routers
* Intrusion detection systems

The technology should also support a quick response when security is compromised. 

---

## 4. Time

**Time** is another dimension of the cybersecurity architecture. At any particular time, information may be available **online or offline**, and systems and information may be changing. This can create opportunities for unauthorized access. 

Therefore, security must be maintained continuously throughout the **storage, processing, and transmission** of information.

---

## 5. Overall Architecture

The architecture can be represented simply as:

```text
                 CYBERSECURITY / INFORMATION ASSURANCE
                              │
          ┌───────────────────┼───────────────────┐
          │                   │                   │
   Information States   Security Services   Countermeasures
          │                   │                   │
   ┌──────┼──────┐      ┌─────┼─────┐       ┌────┼────┐
   │      │      │      │     │     │       │    │    │
Storage Processing Transmission CIA +    People Policy Technology
                              Authentication
                              + Non-repudiation
                              │
                            Time
```

The diagram in the PDF presents these dimensions together, showing how **information states, security services, and security countermeasures** work across time to protect information. 

## Conclusion

The cybersecurity architecture provides a **layered approach to protecting information**. Information must be protected in its three states—**storage, processing, and transmission**. The five security services—**confidentiality, integrity, availability, authentication, and non-repudiation**—define what protection is required. These are supported by **people, policies and practices, and technology**, while security must be maintained continuously over time. 

This architecture helps organizations maintain the **security, reliability, and trustworthiness of information** throughout its lifecycle.
