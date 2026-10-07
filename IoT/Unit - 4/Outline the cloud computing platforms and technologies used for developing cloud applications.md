# Cloud Computing Platforms and Technologies for Developing Cloud Applications

> **Note:** This answer is drawn from the PDF's *Cloud Platforms*, *AWS*, *Azure*, *GCP*, *Google APIs*, *Service Model*, and *Virtualization* sections.

## 1. Introduction

Cloud platforms are the **infrastructure and software environments that power cloud computing services**. They provide servers, storage, databases, and networking over the Internet instead of on-premises. Developers can build, deploy, and manage applications on them without buying or maintaining hardware.

**What cloud platforms do:**
- **Host computing resources:** servers, storage, networking, and the software environment to run applications.
- **Enable on-demand access:** resources are used on a pay-as-you-go basis with no upfront investment.
- **Offer service models:** IaaS, PaaS, and SaaS.

**Key characteristics:** scalability, cost-effectiveness, accessibility from anywhere, and flexibility.

## 2. Types of Cloud Platforms

| Type | Description |
|---|---|
| **Public cloud platforms** | AWS, Microsoft Azure, Google Cloud Platform (GCP) |
| **Private cloud platforms** | Dedicated to a single organization, with greater control and customization |
| **Hybrid cloud platforms** | Combine public and private environments for a flexible approach |

## 3. Amazon Web Services (AWS)

- Launched in **2006** by Amazon.com. It is described as the world's most comprehensive and widely adopted cloud platform.
- Offers computing power, storage, networking, databases, machine learning, and **200+ services**.
- **Characteristics:** scalable, pay-as-you-go, global infrastructure, secure, highly available, broad service offering.

| Category | Service | Description |
|---|---|---|
| Compute | **EC2** | Virtual servers to run applications |
| Compute | **Lambda** | Serverless computing |
| Storage | **S3** | Object storage |
| Database | **RDS** | Managed SQL databases |
| Database | **DynamoDB** | NoSQL database |
| Networking | **VPC** | Isolated network space |
| Security | **IAM** | User and access management |

**Use cases:** web hosting, mobile apps, data analytics, ML, IoT, enterprise IT.
**PaaS offering:** AWS Elastic Beanstalk.

## 4. Microsoft Azure

- Developed by Microsoft and launched in **2010**.
- Used to build, deploy, and manage applications through Microsoft-managed data centres. It supports multiple languages and tools, both Microsoft and third-party.
- **Characteristics:** integrated with Microsoft tools, hybrid cloud capabilities, scalable and flexible, enterprise-friendly, compliance-ready.

| Category | Service | Description |
|---|---|---|
| Compute | **Virtual Machines** | Scalable virtual servers |
| Compute | **Azure Functions** | Serverless compute |
| Storage | **Blob Storage** | Object storage |
| Database | **SQL Database** | Managed SQL database |
| Database | **Cosmos DB** | NoSQL database |
| Networking | **Virtual Network** | Private networking |
| Security | **Azure AD** | Identity and access management |

**Use cases:** Windows workloads, hybrid cloud, AI, DevOps, IoT.

## 5. Google Cloud Platform (GCP)

- Google's suite of cloud services, launched in **2008**.
- Known for excellence in **data analytics, machine learning**, and support for open-source tools such as **Kubernetes and TensorFlow**.
- **Characteristics:** data and ML centric, open-source friendly, high-performance global network, Google Workspace integration.

| Category | Service | Description |
|---|---|---|
| Compute | **Compute Engine** | Virtual machines |
| Compute | **Cloud Functions** | Serverless computing |
| Storage | **Cloud Storage** | Object storage |
| Database | **Cloud SQL** | Managed SQL databases |
| Database | **Firestore** | NoSQL document DB |
| Networking | **VPC Network** | Isolated network space |
| AI/ML | **Vertex AI** | End-to-end ML lifecycle platform |

**Use cases:** big data, AI/ML, Kubernetes hosting, SaaS apps.
**PaaS offering:** Google App Engine, which supports Python, Java, and Go.

## 6. Cross-Platform Comparison

| Feature | AWS | Azure | GCP |
|---|---|---|---|
| **Launched** | 2006 | 2010 | 2008 |
| **Virtual machines** | EC2 | Virtual Machines | Compute Engine |
| **Serverless** | Lambda | Azure Functions | Cloud Functions |
| **Object storage** | S3 | Blob Storage | Cloud Storage |
| **SQL database** | RDS | SQL Database | Cloud SQL |
| **NoSQL database** | DynamoDB | Cosmos DB | Firestore |
| **Networking** | VPC | Virtual Network | VPC Network |
| **Identity** | IAM | Azure AD | (not listed in the PDF) |
| **Strength** | Breadth of services | Microsoft/hybrid integration | Data, ML, open source |

## 7. Technologies Used for Developing Cloud Applications

### 7.1 Virtualization
- A **hypervisor** creates multiple VMs on one physical machine, each with its own OS and applications.
- It is the foundation of IaaS.
- Server-virtualization software includes **VMware vSphere, Microsoft Hyper-V, and KVM**.
- Types: application, network, desktop, storage, server, and data virtualization.

### 7.2 Service-Model Technologies

| Model | Technologies / Platforms | Developer Benefit |
|---|---|---|
| **IaaS** | AWS EC2, Google Compute Engine, Azure VMs | Full control over OS and applications |
| **PaaS** | Heroku, Google App Engine, AWS Elastic Beanstalk | Build and deploy without managing infrastructure |
| **SaaS** | Salesforce, Google Workspace, Microsoft 365 | Ready-to-use applications |

PaaS use cases include web app development, API management, and microservices architecture.

### 7.3 Serverless Computing
- **AWS Lambda, Azure Functions, and Google Cloud Functions** run code without managing servers.

### 7.4 Storage and Database Technologies
- **Object storage:** S3, Blob Storage, Cloud Storage.
- **Relational (SQL):** RDS, Azure SQL Database, Cloud SQL.
- **NoSQL:** DynamoDB, Cosmos DB, Firestore.

### 7.5 Open-Source and AI/ML Technologies
- **Kubernetes** for hosting and container orchestration.
- **TensorFlow** for machine learning.
- **Vertex AI** for the ML lifecycle.

### 7.6 Google APIs

Google APIs let third-party applications communicate with and extend Google services such as Search, Gmail, Translate, and Maps.

- **Authentication:** all APIs use the **OAuth 2.0** protocol.
  1. Obtain credentials from the Developers Console.
  2. The client app requests an access token from the Google Authorization Server.
  3. The token is used to access the Google API service.
- **Client libraries:** Java, JavaScript, Node.js, Objective-C, Go, Dart, Ruby, .NET, PHP, and Python.
- **Google Loader:** a JavaScript library for loading Google APIs dynamically.
- **Google Apps Script:** a cloud-based JavaScript platform to automate Calendar, Docs, Drive, Gmail, and Sheets, and to create add-ons.

**Common application uses:**
- **Sign in with Google:** quick, secure login for Android and web apps.
- **Drive apps:** web apps for collaborative editing, working entirely in the cloud.
- **Custom Search API:** a search box embedded in a website.
- **Maps APIs:** embedded Google maps using the Static Maps, Places, and Earth APIs.
- **App Engine apps:** PaaS-hosted web apps running in Google data centres.

## 8. Advantages of Using Cloud Platforms for Development

- **Cost:** no capital expenditure on hardware or software.
- **Speed:** resources are available in minutes.
- **Scalability:** resources scale up or down on demand.
- **Productivity:** no patching or hardware maintenance.
- **Reliability:** fast and inexpensive backup and recovery.
- **Security:** vendor-provided policies and controls.

## 9. Conclusion

Cloud application development rests on three public cloud platforms, **AWS, Microsoft Azure, and Google Cloud Platform**, each offering compute, storage, database, networking, and security services. Supporting technologies include **virtualization, IaaS/PaaS/SaaS models, serverless computing, Kubernetes, and Google APIs with OAuth 2.0**. Together they let developers build scalable, cost-effective, and highly available applications without managing physical infrastructure.
