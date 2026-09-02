# IoT Complete Architectural Stack – 13 Marks

## 1. Introduction

The **IoT Complete Architectural Stack** explains how IoT devices collect data, communicate it, process it and provide services to users. The architecture in the PDF is based on a **Service-Oriented Architecture (SOA)** and contains four main layers: **Sensing, Networking, Service and Interface**. Security is a common requirement across all layers. 

## 2. Neat Diagram

```text
              ┌──────────────────────────────┐
              │       INTERFACE LAYER        │
              │ Application | API | Interface│
              │         Service Bus          │
              └──────────────┬───────────────┘
                             ↕
              ┌──────────────────────────────┐
              │        SERVICE LAYER         │
              │ Service Division/Integration│
              │ Repository | Business Logic  │
              │          Service Bus          │
              └──────────────┬───────────────┘
                             ↕
              ┌──────────────────────────────┐
              │       NETWORKING LAYER       │
              │ Internet | WLAN | WSN        │
              │ Mobile Network | Database    │
              └──────────────┬───────────────┘
                             ↕
              ┌──────────────────────────────┐
              │        SENSING LAYER         │
              │ RFID | Sensors | BLE | WSN   │
              │      Data Sensing Protocols  │
              └──────────────────────────────┘

                  ║ SECURITY – ALL LAYERS ║
```

---

## 3. Sensing Layer

The **Sensing Layer** is the bottom layer and interacts with the physical environment.

**Functions:**

* Collects data using sensors and RFID technologies.
* Converts physical conditions into signals/data.
* Sends collected data to higher layers.

**Components:** RFID tags, intelligent sensors, RFID readers, BLE devices and WSNs. 

**Example:** Temperature and humidity sensors collect environmental data.

---

## 4. Networking Layer

The **Networking Layer** connects IoT devices and enables them to exchange information.

**Functions:**

* Connects different devices.
* Transfers sensor data over networks.
* Collects information from existing IT infrastructure.

**Technologies:** Internet, WLAN, WSN, mobile networks and databases. It can also connect systems such as healthcare, power grids and transportation systems. 

---

## 5. Service Layer

The **Service Layer** works as middleware between networks and applications.

**Main components:**

* Service Division
* Service Integration
* Service Repository
* Service Bus
* Business Logic

**Functions:**

* Integrates different IoT services.
* Provides reusable services.
* Processes data and applies business logic.
* Connects applications with IoT devices.

The middleware provides an efficient and reusable platform for IoT services. 

---

## 6. Interface Layer

The **Interface Layer** is the top layer and provides interaction between IoT services and applications/users.

**Components:**

* Application Frontend
* Contract
* Interface
* Application API
* Service Bus

**Functions:**

* Provides access to IoT services.
* Simplifies device/service management.
* Allows applications to interact with IoT devices through interfaces and APIs. 

---

## 7. Security

**Security** applies across the entire IoT architecture. It protects devices, communication, services and user data from unauthorized access and attacks. Security is one of the major challenges of IoT. 

---

## 8. Working of IoT Stack

```text
Physical Environment
        ↓
Sensors / RFID / BLE
        ↓
Sensing Layer
        ↓
Internet / WLAN / WSN
        ↓
Networking Layer
        ↓
Services + Business Logic
        ↓
Service Layer
        ↓
API / Application
        ↓
User / IoT Application
```

The sensor data is collected, transmitted through the network, processed by services and finally presented to the user/application. Based on the decision, actuators can also change the physical environment. 

### Example

In a smart cooling system, a **DHT sensor** measures temperature. If the temperature exceeds **30°C**, the system activates a fan through a relay. 

## 9. Conclusion

The IoT Complete Architectural Stack provides a systematic structure for IoT systems. The **Sensing Layer collects data, Networking Layer communicates it, Service Layer processes and manages services, and Interface Layer connects applications/users**. Security protects the complete stack.
