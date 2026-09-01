# Intrusion Detection System (IDS) – 13 Mark Answer

## 1. Definition

An **Intrusion Detection System (IDS)** is a security system that monitors **network traffic or system activities** to detect malicious or suspicious activities. When an intrusion is detected, it sends an **alert to the administrator**. 

---

## 2. Working of IDS

The basic working of an IDS is:

**Monitor Traffic → Analyze Activity → Compare with Rules/Patterns → Detect Intrusion → Generate Alert**

* IDS continuously monitors network traffic.
* It analyzes data for suspicious or abnormal behavior.
* The activity is compared with predefined rules, patterns or known attack signatures.
* If an attack is detected, an alert is sent to the administrator.
* The administrator investigates and takes necessary action.  

---

## 3. Types of IDS

### 1. Network Intrusion Detection System (NIDS)

NIDS monitors traffic across a **network or subnet**. It checks passing traffic against known attacks and alerts the administrator when suspicious activity is detected. 

### 2. Host Intrusion Detection System (HIDS)

HIDS runs on an individual **host or device**. It monitors incoming and outgoing traffic and checks system files for unauthorized modifications. 

### 3. Hybrid IDS

A Hybrid IDS combines **host information and network information** to provide a more complete view of the system. **Prelude** is an example mentioned in the document. 

### 4. Application Protocol-Based IDS (APIDS)

APIDS monitors and interprets **application-specific protocols**. For example, it can monitor **SQL communication** between a web server and database. 

### 5. Protocol-Based IDS (PIDS)

PIDS monitors the communication protocol between a **user/device and a server**. It can monitor protocols such as **HTTPS/HTTP** to protect web servers. 

---

## 4. Detection Methods

### A. Signature-Based Detection

It compares network packets with a database of **known attack signatures**.

**Advantage:** Easily detects known attacks.
**Limitation:** Cannot easily detect new attacks whose signatures are not yet known. 

### B. Anomaly-Based Detection

It creates a model of **normal system activity** and identifies activity that differs from this model. Machine learning can be used to build the activity model, making it useful for detecting unknown attacks. 

---

## 5. IDS Evasion Techniques

Attackers may try to avoid IDS detection using:

* **Fragmentation** – Dividing packets into smaller pieces.
* **Packet Encoding** – Encoding malicious content using methods such as Base64 or hexadecimal.
* **Traffic Obfuscation** – Making malicious traffic difficult to interpret.
* **Encryption** – Hiding malicious content through encryption. 

---

## 6. IDS vs Firewall

| IDS                                                   | Firewall                                            |
| ----------------------------------------------------- | --------------------------------------------------- |
| Detects and reports suspicious activity.              | Restricts or blocks unauthorized access.            |
| Mainly generates alerts after detecting an intrusion. | Attempts to prevent unwanted traffic from entering. |
| Provides monitoring and detection.                    | Provides access control.                            |

The document explains that a firewall restricts access between networks, while an IDS **detects suspected intrusions and raises an alarm**. 

---

## 7. Placement of IDS

The common placement of an IDS is **behind the firewall**, where it can monitor incoming network traffic. IDS can also be placed **within the network** to detect suspicious internal activities and attackers moving through the network. 

---

## 8. Benefits of IDS

* Detects malicious and suspicious activities.
* Alerts administrators before major damage occurs.
* Helps identify network weaknesses.
* Improves network security.
* Helps meet compliance requirements through monitoring and reporting. 

## Conclusion

An **Intrusion Detection System** is an important security mechanism that continuously monitors systems and networks for attacks. By using **signature-based and anomaly-based detection**, different types of IDS can identify both known and unusual threats and alert administrators for further action.
