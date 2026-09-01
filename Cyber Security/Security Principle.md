## Security Principles – 13 Mark Answer

According to the given **Unit-1 PDF**, Microsoft Windows follows several core security principles to protect users, devices, and data from **unauthorized access, malware, and system breaches**. 

### 1. Principle of Least Privilege (PoLP)

The **Principle of Least Privilege** means that users and processes should have **only the permissions required to perform their tasks and nothing more**.

* It reduces the possible damage caused by malware or user mistakes.
* Users cannot perform administrative operations unless they have the required privileges.
* **Example:** A normal user cannot install software without administrator rights.

Thus, least privilege limits unauthorized access and reduces security risks. 

### 2. User Account Control (UAC)

**User Account Control (UAC)** ensures that applications normally run with **standard user privileges** unless the user explicitly approves administrator-level access.

* It helps prevent unauthorized changes to the system.
* Windows displays a confirmation prompt when an application requires administrative privileges.
* **Example:** When an application tries to install software, Windows asks the user for permission.

UAC therefore provides an additional security check before sensitive system changes are made. 

### 3. Secure by Default

The **Secure by Default** principle means that Windows components and services are configured in the **most secure mode by default**.

* It reduces security weaknesses caused by incorrect configuration.
* Users do not have to manually configure every basic security feature.
* **Example:** Windows Firewall is enabled automatically.

This principle helps protect systems even when users do not make additional security configurations. 

### 4. Defense in Depth

**Defense in Depth** uses **multiple layers of security** so that if one security mechanism fails, other mechanisms can still protect the system.

Important security components include:

* Antivirus
* Firewall
* Secure Boot
* SmartScreen
* BitLocker
* UAC

**Example:** If malware bypasses a browser security mechanism, antivirus and UAC may still detect or block it. 

Therefore, defense in depth prevents dependence on a single security mechanism.

### 5. Identity and Access Management

Windows uses **authentication and authorization** to ensure that users are really who they claim to be and that they receive appropriate access.

Technologies mentioned in the document include:

* Windows Hello
* Active Directory
* Azure AD
* PIN
* Biometrics

Its purpose is to provide **secure and flexible login options** while controlling access to system resources. 

### 6. Patch Management

**Patch Management** involves providing regular security updates through **Windows Update**.

* It fixes security vulnerabilities quickly.
* It helps prevent attackers from exploiting known weaknesses.
* **Example:** Microsoft provides regular updates through **Patch Tuesday**.

Regular patching is important because outdated software may contain vulnerabilities that attackers can exploit.

### Conclusion

The major Windows security principles are **Least Privilege, User Account Control, Secure by Default, Defense in Depth, Identity and Access Management, and Patch Management**. Together, these principles provide multiple layers of protection against unauthorized access, malware, system changes, and security vulnerabilities. They help maintain a secure Windows environment by combining **proper permissions, authentication, secure configuration, multiple security layers, and regular updates**. 

**Exam tip:** For a 13-mark answer, write the **6 principles with definition + purpose/example** and finish with the conclusion. This is a good medium-length answer based only on your PDF.
