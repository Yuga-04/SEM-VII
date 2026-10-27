# Evading Detection and Elevating Privileges – 13 Mark Answer

## 1. Introduction

In cybersecurity, attackers commonly use two important techniques:

* **Evading Detection** – Hiding malicious activities from security systems.
* **Elevating Privileges** – Gaining higher access rights than originally provided.

These techniques are important stages in the **Cyber Attack Lifecycle / MITRE ATT&CK framework**. 

---

## 2. Evading Detection

### Meaning

Evading detection refers to techniques used by attackers or malware to avoid being identified by **antivirus, IDS/IPS, firewalls and monitoring systems**. 

### Common Techniques

1. **Obfuscation / Encryption** – Hides malicious code from signature-based detection.
2. **Polymorphism and Metamorphism** – Changes the structure or code of malware during infections.
3. **Rootkits** – Modify OS functions to hide files and processes.
4. **Living-off-the-Land (LOL) Binaries** – Uses legitimate system tools such as **PowerShell and WMI** to avoid suspicion.
5. **Anti-VM / Anti-Debugging** – Detects sandboxes or virtual machines and changes its behavior.
6. **Log Tampering** – Deletes or modifies event logs to remove evidence. 

### Impact

Successful detection evasion gives attackers more time to **move through the network, steal data and deploy additional malicious payloads**. 

---

## 3. Elevating Privileges

### Meaning

Privilege escalation means exploiting vulnerabilities or misconfigurations to obtain **higher access rights**, such as moving from a normal user to an administrator or root user. 

### Types

1. **Vertical Privilege Escalation** – A normal user gains higher privileges, such as **user → administrator**.
2. **Horizontal Privilege Escalation** – A user accesses another user's data or resources at the same privilege level. 

### Common Techniques

* **Exploiting software bugs** – Using kernel or OS vulnerabilities.
* **Credential Theft** – Stealing passwords, tokens or hashes.
* **Misconfigurations** – Exploiting weak permissions or unpatched systems.
* **Pass-the-Hash / Pass-the-Ticket** – Using stolen authentication material.
* **Abusing SUID/Setuid binaries** – Executing privileged code in Linux. 

### Impact

Privilege escalation can allow attackers to gain **full system control**, disable security defenses, steal sensitive information and spread across the network. 

---

## 4. Detection and Defense

### Against Detection Evasion

* Use **behavior-based and anomaly detection**.
* Deploy **EDR and SIEM** for monitoring.
* Enable **file integrity monitoring**.

### Against Privilege Escalation

* Apply regular **patches and system hardening**.
* Follow the **Principle of Least Privilege (POLP)**.
* Use **Multi-Factor Authentication (MFA)**.
* Regularly audit and monitor administrator activities. 

---

## 5. Examples

* **Stuxnet** used rootkit techniques to hide its processes and evade detection.
* **WannaCry** used the **EternalBlue Windows SMB vulnerability** for admin-level access. 

## Conclusion

**Evading detection** helps attackers remain hidden, while **privilege escalation** gives them greater control over the system. Therefore, behavior monitoring, EDR, regular patching, least privilege and MFA are essential defenses against these attacks.
