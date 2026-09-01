# Rootkits – 13 Mark Answer

## 1. Definition

A **rootkit** is malicious software that allows an attacker to gain **unauthorized remote access and control** over a computer. It is mainly designed to **hide its presence** and maintain access to the system. It can also create a backdoor to install other malware. 

## 2. Types of Rootkits

1. **Bootloader Rootkit** – Infects the boot process and loads before the operating system starts.
2. **Firmware Rootkit** – Hides inside device firmware and is difficult to detect.
3. **Kernel Rootkit** – Attacks the operating system kernel and provides high-level system control.
4. **Memory Rootkit** – Operates in RAM and is usually removed after restarting the system.
5. **Application Rootkit** – Modifies application files and activates when the infected application runs.  

## 3. How Rootkits Work

The main steps are:

**Privilege Escalation → Installation → Hiding → Persistence → Malicious Activities**

* **Privilege Escalation:** Gains higher system privileges.
* **Installation:** Modifies firmware, kernel modules or system files.
* **Hiding:** Conceals files, processes and registry entries.
* **Persistence:** Remains active even after system restart.
* **Malicious Activities:** Steals data, monitors users and installs other malware. 

## 4. Methods of Infection

Rootkits commonly enter through:

* Phishing emails
* Malicious executable files
* Malicious PDF/Word documents
* Infected software
* Compromised shared drives
* Untrusted websites 

## 5. Effects of Rootkits

* Steal sensitive and financial information.
* Monitor user activities and keystrokes.
* Modify or corrupt system files.
* Create backdoors for attackers.
* Reduce system performance.
* Compromise network security. 

## 6. Symptoms

* Slow system performance
* Frequent crashes or unexpected restarts
* Unusual network activity
* Altered or missing files
* Unknown background processes 

## 7. Prevention

* Keep OS and software updated.
* Use reliable antivirus/anti-malware software.
* Use behavior-based detection.
* Perform system integrity checks.
* Follow the **Least Privilege Principle**.
* Avoid suspicious links and downloads. 

## 8. Examples

* **Stuxnet** – Used rootkit techniques against industrial control systems.
* **Alureon (TDSS)** – Avoids detection and modifies system operations.
* **Zeus** – Banking malware using rootkit technology.
* **Rootkit.Reveton** – Ransomware-related rootkit.
* **Carberp** – Steals financial data while avoiding detection. 

## Conclusion

Rootkits are dangerous because they **hide from security software while providing attackers with privileged access**. Regular updates, security software, system monitoring and least-privilege access are important for preventing rootkit attacks.
