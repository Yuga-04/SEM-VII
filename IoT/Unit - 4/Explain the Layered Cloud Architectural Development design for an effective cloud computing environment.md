# Layered Cloud Architectural Development Design

> **Note:** The PDF has no section with this exact title. The layered architecture is covered across its Service Model, Virtualization, and Responsibility Breakdown sections, so this answer is built from those.

## 1. Introduction

Cloud computing delivers servers, storage, databases, networking, software, and analytics over the Internet. It uses a **virtualized platform with elastic resources provisioned on demand**. To do this effectively, the cloud is organised as a **stack of layers**. Each layer hides the complexity of the layer below it (**abstraction**) and offers a service to the layer above.

## 2. Layered Architecture Overview

```
┌──────────────────────────────────────────────┐
│  SaaS  – Software as a Service (Application) │  ← End users
├──────────────────────────────────────────────┤
│  PaaS  – Platform as a Service (Platform)    │  ← Developers
├──────────────────────────────────────────────┤
│  IaaS  – Infrastructure as a Service         │  ← System admins
├──────────────────────────────────────────────┤
│  Virtualization Layer (Hypervisor)           │
├──────────────────────────────────────────────┤
│  Physical Layer (Servers, Storage, Network)  │  ← Data centres
└──────────────────────────────────────────────┘
```

The higher you go in the stack, the more the provider manages and the less control the user has.

## 3. Description of Each Layer

### 3.1 Physical / Hardware Layer
- Consists of physical servers, storage, and networking equipment in **data centres around the world**.
- The **cloud vendor** buys, installs, and maintains this hardware, so users avoid upfront capital costs.

### 3.2 Virtualization Layer
- Uses a **hypervisor** to split one physical server into many **virtual machines (VMs)**, each with its own OS and applications.
- Stack: *Server Hardware → Host OS → Hypervisor → Guest OS → Binaries/Libraries → Application.*
- **Type 1 (bare-metal)** runs directly on hardware and is highly efficient. **Type 2** runs over an installed OS such as Windows or macOS.
- Types of virtualization: application, network, desktop, storage, server, and data.
- Benefits:
  - better resource utilization
  - lower cost
  - flexibility
  - isolation and security
  - easy backup and recovery
- It is the key enabler of IaaS.

### 3.3 Infrastructure as a Service (IaaS)
- Provides virtualized **compute, storage, and networking** on demand.
- **User manages:** guest OS, applications, data, and security. **Provider manages:** virtualization, network, infrastructure, and physical hardware.
- Features: on-demand infrastructure, scalability, pay-as-you-go pricing.
- Use cases: website hosting, disaster recovery, test environments.
- Examples: AWS EC2, Google Compute Engine, Azure VMs.

### 3.4 Platform as a Service (PaaS)
- Provides a platform for developers to **build, deploy, and manage applications** without managing OS, hardware, or network.
- **User manages:** applications and data. **Provider manages:** OS, runtime, middleware, and infrastructure.
- Features: abstraction of infrastructure, built-in scalability, developer tools (APIs, databases, frameworks).
- Use cases: web app development, API management, microservices.
- Examples: Heroku, Google App Engine, AWS Elastic Beanstalk.

### 3.5 Software as a Service (SaaS)
- Provides **fully managed applications** accessed through a web browser, with no installation or maintenance.
- **User manages:** only data and user access. **Provider manages:** everything else.
- Features: vendor-managed updates and patches, subscription pricing, browser-based access.
- Examples: Gmail, Salesforce, Google Workspace, Microsoft 365.

## 4. Responsibility Breakdown Across Layers

| Layer | User Responsibility | Provider Responsibility |
|---|---|---|
| **IaaS** | OS, Applications, Data | Virtualization, Storage, Networking |
| **PaaS** | Applications, Data | OS, Virtualization, Middleware, Networking |
| **SaaS** | Data, User interaction | Everything (OS, Application, Infrastructure) |

Choosing a layer is a trade-off:
- **IaaS:** maximum flexibility and control, but more management.
- **PaaS:** faster development, but less flexibility.
- **SaaS:** minimal effort, but limited customization.

## 5. Deployment Models over the Layers

The layered stack can be deployed in different ways, depending on who owns and controls the infrastructure:
- **Public cloud:** shared, pay-per-use, and no maintenance, but less secure and less customizable.
- **Private cloud:** a dedicated environment with better control, security, and customization, but costly and less scalable.
- **Hybrid cloud:** combines public and private clouds, giving flexibility and cost savings but harder to manage.
- **Community cloud:** shared by organizations with common concerns; cost-effective but less scalable.
- **Multi-cloud:** uses multiple public cloud providers for high availability and reduced latency, but is more complex.

## 6. Key Design Characteristics for an Effective Cloud Environment

According to NIST, a cloud environment must provide five essential characteristics:
1. **On-demand self-service**
2. **Broad network access**
3. **Resource pooling** (multi-tenancy through virtualization)
4. **Rapid elasticity**
5. **Measured service** (pay-per-use)

Further qualities:
- Scalability and agility.
- Device and location independence.
- High availability through redundant sites.
- Centralized security.
- Abstracted and virtualized resources.

## 7. Advantages of the Layered Design

- **Cost:** removes huge capital expenditure on hardware and software.
- **Speed:** resources are available in minutes.
- **Scalability:** resources can be increased or decreased as needed.
- **Productivity:** no patching or hardware maintenance, so IT teams focus on business goals.
- **Reliability:** backup and disaster recovery are cheaper and faster.
- **Security:** vendors provide policies, technologies, and controls that strengthen data security.

## 8. Cloud Platforms Implementing the Layered Model

| Platform | IaaS | PaaS/Serverless | Storage | Database |
|---|---|---|---|---|
| **AWS** | EC2 | Lambda, Elastic Beanstalk | S3 | RDS, DynamoDB |
| **Azure** | Virtual Machines | Azure Functions | Blob Storage | SQL Database, Cosmos DB |
| **GCP** | Compute Engine | Cloud Functions, App Engine | Cloud Storage | Cloud SQL, Firestore |

## 9. Conclusion

The layered cloud architecture runs from **physical hardware → virtualization → IaaS → PaaS → SaaS**. Each layer abstracts the one below it and shifts more management responsibility to the provider. Combined with suitable deployment models (public, private, hybrid, community, or multi-cloud), this design gives a **scalable, flexible, cost-effective, secure, and highly available** cloud computing environment.
