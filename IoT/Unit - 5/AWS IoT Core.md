# AWS IoT Core

**Introduction:** AWS IoT Core is the AWS service that connects IoT devices to other devices and to AWS cloud services. If a device can connect to AWS IoT, AWS IoT can connect it to the cloud services that AWS provides, such as Lambda, S3, DynamoDB and Kinesis. It also provides device software that helps integrate IoT devices into AWS IoT-based solutions.

---

## 1. Architecture
**IoT devices** (sensors, appliances, vehicles, industrial machines) → **AWS IoT Core** → **AWS services** (Lambda, S3, DynamoDB, Kinesis, etc.)

AWS IoT Core acts as the central layer between the devices and the cloud services, handling secure connectivity and message routing.

## 2. Supported Protocols
To manage and support devices in the field, AWS IoT Core supports:
- **MQTT (Message Queuing Telemetry Transport):** lightweight publish/subscribe protocol, ideal for low-bandwidth, high-latency networks.
- **MQTT over WSS (WebSockets Secure):** MQTT over secure WebSockets, used by browser-based web applications.
- **HTTPS (Hypertext Transfer Protocol - Secure):** used by devices and clients to publish messages.
- **LoRaWAN (Long Range Wide Area Network):** for low-power, long-range wireless devices.

## 3. Message Broker
- The AWS IoT Core message broker supports devices and clients using **MQTT and MQTT over WSS** to **publish and subscribe** to messages.
- It also supports clients using **HTTPS** to publish messages.
- Devices publish messages to **topics**; subscribers to those topics receive them in real time.

## 4. AWS IoT Core for LoRaWAN
- Helps connect and manage wireless LoRaWAN devices and gateways.
- It **replaces the need to develop and operate a LoRaWAN Network Server (LNS)**.

## 5. How Devices and Apps Access AWS IoT
| Interface | Purpose |
|---|---|
| **AWS IoT Device SDKs** | Build applications on devices that send and receive messages from AWS IoT |
| **AWS IoT Core for LoRaWAN** | Connect and manage LoRaWAN devices and gateways |
| **AWS CLI** | Run AWS IoT commands on Windows, macOS and Linux |
| **AWS IoT API** | Build IoT applications using HTTP/HTTPS requests |
| **AWS SDKs** | Language-specific APIs that wrap the HTTP/HTTPS API, allowing programming in any supported language |

## 6. Connecting a Web Application to AWS IoT Using MQTT
**Step 1: Create an AWS IoT Thing**
- AWS IoT Core Console → Manage → Things → Create Thing.
- Name it (e.g., webClientThing) and download the certificates and private key.

**Step 2: Attach a Policy**
- Create an IoT policy allowing `iot:Connect`, `iot:Publish`, `iot:Subscribe`, `iot:Receive`.
- Attach the policy to the certificate.

```json
{
  "Version": "2012-10-17",
  "Statement": [{
    "Effect": "Allow",
    "Action": ["iot:Connect", "iot:Publish", "iot:Subscribe", "iot:Receive"],
    "Resource": ["*"]
  }]
}
```

**Step 3: Configure an MQTT Client in the Web App**
- Use the AWS IoT Device SDK for JavaScript or the Paho MQTT client.
- Connect using the secure WebSocket protocol (`wss`) with the IoT endpoint, region and client ID.
- On connect, subscribe and publish to a topic (e.g., `iot/webapp/topic`).

**Step 4: Test with the MQTT Test Client**
- AWS Console → AWS IoT Core → MQTT Test Client → subscribe to the topic.
- Messages from the web app appear in real time.

## 7. Security in AWS IoT Core
| Concern | Mitigation |
|---|---|
| Data confidentiality | TLS encryption (MQTT over SSL/WSS), IAM roles, KMS for encryption at rest |
| Authentication and authorization | X.509 certificates, IAM policies, Cognito Identity Pools |
| Data integrity | Hashing (SHA-256) and digital signatures |
| Device identity spoofing | Unique certificate per device, mutual TLS authentication |
| Denial of Service | Rate limiting, AWS WAF, IoT Device Defender |

## 8. Related AWS IoT Services
- **AWS IoT Greengrass:** runs local compute and ML on edge devices.
- **AWS IoT Analytics:** processes and analyzes IoT data.
- **AWS IoT Device Management:** manages and updates large IoT fleets.

## 9. Example Flow
IoT sensor → publishes via MQTT → **AWS IoT Core** → **Lambda** (processing) → **S3 / DynamoDB** (storage) → dashboard or alert.

---

## Conclusion
AWS IoT Core provides secure, scalable, two-way communication between IoT devices, web applications and AWS services. With support for MQTT, WSS, HTTPS and LoRaWAN, a publish/subscribe message broker, certificate-based security and multiple access interfaces, it forms the core of cloud-based IoT solutions on AWS.
