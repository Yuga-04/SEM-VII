# Automated Malicious Code Analysis – 13 Mark Answer

## 1. Definition

An **Automated Malicious Code Analysis System (AMCAS)** uses automated techniques to **analyze and classify malware**. It reduces the limitations of manual analysis and helps security teams handle the rapidly increasing number of malicious code samples. 

## 2. Main Analysis Techniques

### 1. Static Analysis

Static analysis examines a malicious file **without executing it**.

* **PE Header Analysis** – Examines imports, exports and compiler information.
* **String Extraction** – Finds readable strings such as IP addresses, domains and filenames.
* **Hashing and Signature Matching** – Calculates the file hash and compares it with known malware databases. 

### 2. Dynamic Analysis

Dynamic analysis executes malware safely inside an isolated **sandbox** and observes its actual behavior.

* **Behavior Monitoring** – Observes file-system, registry and process changes.
* **Network Analysis** – Monitors communication with networks and **C2 servers**.
* **Memory Forensics** – Examines memory during execution to identify techniques such as process injection. 

### 3. Hybrid Analysis

Hybrid analysis combines **static and dynamic analysis** to obtain deeper information about malware behavior and intent. 

---

## 3. Working of Automated Malware Analysis

The typical process is:

**Submission → Triage → Sandbox Execution → Behavioral Capture → Report Generation → Threat Intelligence**

1. **Submission:** A suspicious file is submitted manually or automatically.
2. **Triage:** A quick static scan is performed and known malware hashes are identified.
3. **Sandbox Execution:** The suspicious program is executed in a controlled environment.
4. **Behavioral Capture:** API calls, file changes and network activity are recorded.
5. **Report Generation:** Static and dynamic results are combined into a report.
6. **Threat Intelligence:** Indicators of compromise (IOCs), such as C2 IP addresses, and signatures such as **YARA rules** are generated. 

## 4. Advantages

* **Scalability** – Can analyze a large number of malware samples.
* **Speed** – Performs analysis much faster than manual methods.
* **Safety** – Malware can be executed in an isolated environment without infecting the host system.
* **Automation** – Reduces the need for continuous manual analysis.
* **Threat Intelligence** – Quickly produces IOCs and detection signatures. 

## 5. Limitations

Sophisticated malware may use **obfuscation, anti-VM techniques and delayed execution** to avoid analysis. Malware can detect virtual environments by checking system resources, VM-specific files, registry entries and timing differences. 

## Conclusion

Automated malicious code analysis provides a **fast, scalable and safe method** for analyzing malware. By combining static, dynamic and hybrid techniques, AMCAS helps security teams understand malware behavior, identify threats and generate useful threat intelligence for future detection.
