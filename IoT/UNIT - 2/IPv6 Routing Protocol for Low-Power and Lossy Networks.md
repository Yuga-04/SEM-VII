# RPL – IPv6 Routing Protocol for Low-Power and Lossy Networks

### 13-Mark Answer

## 1. Introduction

**RPL (Routing Protocol for Low-Power and Lossy Networks)** is an IPv6 routing protocol designed for **resource-constrained IoT and wireless sensor networks**. It supports **many-to-one and one-to-one communication** and forms a tree-like topology called **DODAG**. RPL was standardized by the IETF ROLL group as **RFC 6550**. 

## 2. RPL Architecture

```text
             DODAG Root / Sink
                    │
             ┌──────┴──────┐
             │              │
           Node 1         Node 2
          /     \            │
       Node 3  Node 4       Node 5
          │
       Sensors
```

* **DODAG Root:** Main destination or sink.
* **IoT Nodes:** Act as routers and form a mesh network.
* **Parent Nodes:** Provide paths towards the root.
* **Objective Function (OF):** Selects the best/optimized route.
* **IPv6 Layer:** Performs routing and determines the next hop. 

## 3. DODAG Formation

A **DODAG (Destination Oriented Directed Acyclic Graph)** is a directed graph with **no routing loops**, oriented towards a root node. 

The formation process is:

1. A **border router/sink** becomes the DODAG root.
2. The **Objective Function** determines how routes are optimized.
3. Nearby nodes join the DODAG by selecting suitable **parent nodes**.
4. Each node can maintain up to **three parents**, with one normally chosen as the **preferred parent**.
5. Parent-child relationships form the complete DODAG.
6. The structure ensures **loop-free upward routing** towards the root. 

## 4. Modes of RPL

### A. Storing Mode

* Nodes maintain routing information for the RPL domain.
* Requires more **memory and processing**.

### B. Non-Storing Mode

* Complete routing information is maintained by the **border router/root**.
* Other nodes mainly maintain their parent information.
* Saves **memory and CPU** in constrained devices. 

## 5. Features

* **Scalability** – Supports large IoT networks.
* **Low-power operation** – Suitable for resource-constrained devices.
* **Adaptive routing** – Responds to link quality and energy changes.
* **QoS support** – Supports reliable delivery and congestion control.
* **Mesh networking** – Nodes can act as routers.
* **Loop-free routing** – DODAG avoids routing loops.
* **Security** – Supports integrity, authentication, confidentiality and encryption. 

## 6. Advantages

* Efficient for **low-power and lossy networks**.
* Reduces routing overhead and resource usage.
* Supports **large-scale IoT networks**.
* Provides reliable and adaptive communication.
* Saves memory using **non-storing mode**.
* Suitable for **wireless sensor and IoT applications**.

## 7. Conclusion

RPL is an important **IPv6 routing protocol for IoT networks**. Its **DODAG-based architecture, two operating modes, scalability, adaptive routing and low-resource requirements** make it suitable for constrained wireless IoT environments. 
