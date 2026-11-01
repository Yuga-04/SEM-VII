# Design a Secure IoT Framework for a Smart City Surveillance System – Transport, Identification and Privacy Management Protocols (13 Marks)

## 1. Introduction

A Smart City Surveillance System uses IoT devices such as CCTV cameras, sensors and connected monitoring devices to collect and transmit real-time information for public safety and security.

However, these devices may be vulnerable to cyberattacks, unauthorized access, data theft and privacy violations.

Therefore, a secure IoT framework is required to ensure:

1. Secure communication between IoT devices.
2. Unique identification and authentication of devices.
3. Protection of personal and surveillance data.
4. Prevention of unauthorized access.
5. Secure storage and transmission of information.

The framework uses transport, identification and privacy management protocols to provide secure communication and data protection.

## 2. Architecture of Secure IoT Framework

[Internet of Things for Enhancing Public Safety, Disaster Response, and Emergency Management](https://images.openai.com/static-rsc-4/yBHZyKramZhsgqNQzMKLsjqIKWlEHw-GEv2xltToITL6YpwNlDlj-mlcB6CQIROGbEAuB65WjBjSeXIO7E-5r9xkByipNQadvS8dZaw-PHmaI28EyjDW0zfatlsbbko6iR79ueVo0T0wTxmqwPI6DWDyB25G2r4zfZUiLRcBWsY?purpose=inline)

[mdpi.com](https://www.mdpi.com/2673-4591/92/1/61?utm_source=chatgpt.com)

The architecture consists of the following layers:

1\. Perception Layer

- Contains CCTV cameras, motion sensors, traffic cameras and environmental sensors.
- Collects real-time images, videos and sensor information.
- Uses unique device identities to identify each connected device.

2\. Network and Transport Layer

- Transfers collected data from IoT devices to gateways and cloud servers.
- Uses Wi-Fi, Li-Fi and Bluetooth Low Energy (BLE) for wireless communication.
- Uses secure transport protocols such as TLS and DTLS to protect data.

3\. Identification Layer

- Provides a unique identity to every IoT device.
- Uses Uniform Resource Identifiers (URIs) and IP addresses to identify devices and resources.
- Ensures that only authenticated devices can participate in the network.

4\. Cloud and Processing Layer

- Receives and stores surveillance data.
- Processes video streams and sensor information.
- Performs monitoring, analysis and alert generation.
- Applies access control and encryption to protect stored information.

5\. Application Layer

- Provides a dashboard for authorized security personnel.
- Displays live CCTV footage, alerts and monitoring information.
- Allows authorized users to access surveillance information securely.

## 3. Transport Protocols

Transport protocols enable communication between surveillance cameras, sensors, gateways and cloud servers.

The following transport technologies are used:

### A. Wi-Fi (Wireless Fidelity)

- Provides wireless communication with good range and high bandwidth.
- Supports transmission of large amounts of data, including CCTV images and video.
- Widely used in smart city infrastructure.
- It may be affected by interference and consumes more power than some alternatives.
- Security should be strengthened using WPA2/WPA3 and encrypted communication.

### B. Li-Fi (Light Fidelity)

- Uses light waves instead of radio frequencies to transmit data.
- Provides high-speed data transmission.
- Offers secure communication because light does not penetrate walls.
- Suitable for sensitive environments.
- Its limitation is that it requires direct line of sight or light reflection.

### C. BLE (Bluetooth Low Energy)

- Provides short-range wireless communication with low power consumption.
- Suitable for connecting small sensors and monitoring devices.
- Used for indoor positioning and asset tracking.
- It has a limited communication range and lower data transfer rates compared to Wi-Fi and Li-Fi.

### Comparison of Transport Protocols

| Feature           | Wi-Fi           | Li-Fi                     | BLE                  |
| ----------------- | --------------- | ------------------------- | -------------------- |
| Communication     | Radio waves     | Light waves               | Radio waves          |
| Range             | Good            | Limited                   | Short                |
| Speed             | High            | Very high                 | Low                  |
| Power consumption | Relatively high | Depends on infrastructure | Low                  |
| Main application  | CCTV cameras    | Secure data transfer      | Sensors and tracking |

## 4. Identification Protocols – URI

### Definition

A Uniform Resource Identifier (URI) is a unique sequence of characters used to identify a physical or logical resource in a network.

In a smart city surveillance system, URIs help uniquely identify cameras, sensors, video resources and other connected devices.

### Types of URI

1\. Uniform Resource Locator (URL)

- Identifies the location of a resource on a network.
- Specifies how to access the resource.
- Example: An HTTPS address used to access a surveillance camera's authorized video stream.

2\. Uniform Resource Name (URN)

- Provides a unique and permanent name for identifying a resource.
- It does not depend on the physical location of the resource.
- Example: A permanent identifier assigned to a registered CCTV camera.

3\. Uniform Resource Characteristics (URC)

- Provides metadata describing the properties of a resource.
- Includes information such as encoding and access restrictions.
- Helps describe surveillance resources and their characteristics.

### Importance of URI in Smart City Surveillance

1. Provides unique identification for connected devices.
2. Helps locate and access surveillance resources.
3. Supports communication between different IoT devices.
4. Organizes and categorizes cameras and sensor information.
5. Improves device management and interoperability.

## 5. Privacy Management and Security Protocols

IoT privacy refers to protecting personal and sensitive information collected by connected devices.

In smart city surveillance, cameras may collect images, videos, vehicle details and other personal information. Therefore, proper security mechanisms are required.

### A. Major Security Threats

The following are common security attacks in IoT:

1. Software Attacks: Attackers exploit vulnerabilities in device software.
2. Inadequate Physical Security: Attackers physically modify devices or install malicious software.
3. Communication Attacks: Attackers intercept or manipulate data transmitted between devices.
4. Data Security Attacks: Unauthorized users access sensitive personal information.
5. Low Visibility: Organizations may fail to identify all devices connected to their networks.

### B. Privacy and Security Solutions

1\. Secure API

- APIs allow IoT devices to exchange information with other systems.
- Secure APIs prevent unauthorized access to surveillance devices.
- API authentication and authorization should be implemented.

2\. Network Visibility

- Maintain an inventory of all connected IoT devices.
- Use Network Access Control (NAC) to identify and monitor devices.
- Detect unknown devices joining the network.

3\. Encrypted Communication

- Encrypt communication between IoT devices, gateways and cloud servers.
- Use SSL/TLS to protect data during transmission.
- Use DTLS for secure communication over UDP.
- Prevent unauthorized users from reading or modifying transmitted information.

4\. Authentication

Authentication ensures that only authorized users and devices can access the surveillance system.

The following methods are used:

- Biometric Authentication: Uses fingerprints or facial recognition to verify authorized users.
- Digital Certificates: Verify the identity of connected devices and servers.
- Multi-Factor Authentication (MFA): Requires multiple verification methods before granting access.

5\. Firewalls and Intrusion Detection

- Firewalls prevent unauthorized network access.
- Intrusion Detection Systems (IDS) identify suspicious activities.
- Antivirus and antimalware protect devices from malicious software.

6\. Access Control

- Implement Role-Based Access Control (RBAC).
- Provide different permissions to administrators, security officers and monitoring staff.
- Restrict access to sensitive video recordings.
- Change default passwords and disable unnecessary remote access.

7\. Security Updates

- Regularly update device firmware and software.
- Apply security patches to fix known vulnerabilities.
- Monitor devices continuously to identify suspicious activities.

## 6. Working of the Secure Smart City Surveillance Framework

The complete working process is as follows:

1\. Data Collection: CCTV cameras and sensors collect real-time surveillance information from different locations.

2\. Device Identification: Each camera and sensor is identified using a unique URI and network address.

3\. Secure Communication: Wi-Fi, Li-Fi or BLE transfers information to IoT gateways. TLS or DTLS protects the communication.

4\. Authentication: Devices and users are verified using digital certificates, passwords or multi-factor authentication.

5\. Data Processing: The gateway and cloud server process the collected information and generate alerts when suspicious activities are detected.

6\. Privacy Protection: Encryption and access control protect sensitive surveillance information from unauthorized access.

7\. Monitoring: Authorized security personnel access live footage and alerts through a secure dashboard.

8\. Continuous Security: Firewalls, intrusion detection systems and regular security updates protect the entire IoT infrastructure.

## 7. Advantages of Secure IoT Framework

1. Data Confidentiality: Protects sensitive surveillance information through encryption.
2. Authentication: Prevents unauthorized devices and users from accessing the system.
3. Data Integrity: Protects information against unauthorized modification.
4. Privacy Protection: Prevents misuse of personal information.
5. Real-Time Monitoring: Enables continuous surveillance of public areas.
6. Scalability: Supports the addition of more cameras and sensors.
7. Reliability: Improves secure communication and system availability.

## 8. Conclusion

A secure IoT framework is essential for smart city surveillance systems to protect sensitive information and ensure reliable communication.

- Transport protocols such as Wi-Fi, Li-Fi and BLE enable wireless communication.
- Identification protocols such as URI provide unique identification of devices and resources.
- Privacy and security mechanisms such as TLS, DTLS, authentication, encryption, firewalls and access control protect sensitive data.

Therefore, integrating these protocols provides a secure, reliable and scalable smart city surveillance system.

## PDF reference – Unit II: Protocols for IoT

The answer is based on the following portions of your uploaded UNIT2.pdf:

| Topic                                          | PDF pages |
| ---------------------------------------------- | --------- |
| IP infrastructure and security protocols       | 1–2       |
| URI identification                             | 3–7       |
| Wi-Fi, Li-Fi and BLE transport                 | 8         |
| CoAP and DTLS security                         | 20–21     |
| IoT privacy, security threats and solutions    | 23–24     |
| IoT security best practices and access control | 26–27     |



UNIT2.pdf

UNIT2.pdf

UNIT2.pdf

UNIT2.pdf

UNIT2.pdf

UNIT2.pdf



Exam tip: For 13 marks, give special importance to the three main headings asked in the question: Transport Protocols, Identification Protocols and Privacy Management Protocols. Draw the secure IoT architecture diagram and explain the working to make the answer complete.
