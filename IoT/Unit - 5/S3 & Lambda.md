# Amazon S3 and AWS Lambda

**Introduction:** Amazon S3 (Simple Storage Service) and AWS Lambda are two core AWS services used in IoT and cloud applications. S3 provides scalable object storage, while Lambda provides serverless compute that processes data without any server management.

---

# PART A: Amazon S3 (Simple Storage Service)

## 1. Overview
- S3 is storage for the internet, with a simple web service interface to store and retrieve any amount of data, anytime, from anywhere.
- It is **object-based storage**; an operating system cannot be installed on it.
- Data is stored redundantly in multiple locations (minimum 3 in the same region).

## 2. Object Storage vs Block Storage
| Block Storage | Object Storage |
|---|---|
| Data divided into evenly sized blocks | Files stored as a whole, not divided |
| No metadata; only the block address is kept | Object = data + metadata + globally unique ID |
| Suited for databases, random read/write | Cannot be mounted as a drive |
| Example: AWS EBS | Examples: AWS S3, Dropbox |

## 3. Buckets
- Data is stored in a **bucket**, a flat container of objects.
- A bucket is region specific; up to 100 buckets per account (can be expanded on request).
- Folders can be created inside a bucket, but nested buckets are not possible.
- Bucket ownership is non-transferable.
- By default, buckets and objects are **private**; only the owner can access them.

**Bucket naming rules:**
- Names are globally unique across all AWS regions and cannot be changed after creation.
- Length must be 3 to 63 characters.
- Only lowercase letters, numbers and hyphens are allowed; no uppercase letters.
- Must not be an IP address; each label must start and end with a lowercase letter or number.

**Sub-resources:** Lifecycle, Website, Versioning, Access Control List (bucket policies).

## 4. Objects
- Size ranges from 0 bytes to 5 TB.
- Each object is identified by: service endpoint, bucket name, object key (name) and optionally the version.
- Objects never leave their region unless moved or replicated (CRR).
- Permissions can be granted to individual users, an AWS account, all authenticated users, or the public.

## 5. Versioning
- Protects against accidental deletion or overwriting; also used for retention and archiving.
- Once enabled it **cannot be disabled, only suspended**.
- On deletion, a **delete marker** is placed; removing the marker restores the object.
- Version states: Enabled, Suspended, Un-versioned.
- All stored versions are charged; lifecycle policies can delete old versions or move them to Glacier.
- **MFA Delete** adds extra security for changing the versioning state and permanently deleting versions. It requires security credentials plus a code from an authentication device.

## 6. Multipart Upload and Copying
- **Multipart upload:** Uploads an object in parts, in parallel and in any order. Recommended for objects of 100 MB or more; **mandatory above 5 GB**.
- **Copy operation:** Single copy supports objects up to 5 GB; larger objects need the multipart API. Uses include renaming, changing storage class, encrypting, moving across regions and changing metadata.

## 7. Storage Classes
| Class | Key Features |
|---|---|
| **S3 Standard** | Frequently accessed data; 99.99% availability; high storage cost, low access cost |
| **S3 Standard-IA** | Infrequent but rapid access; about half the storage price, higher access charges; 99.9% availability |
| **Intelligent Tiering** | Automatically moves data to the most cost-effective tier; no retrieval fees |
| **One Zone-IA** | Stored in a single AZ; cheaper; suitable for re-creatable data and secondary backups |
| **S3 Glacier** | Low-cost archiving; retrieval takes minutes to hours |
| **Glacier Deep Archive** | Cheapest class; long-term retention (e.g., 10 years); retrieval within 12 hours |

Durability for all classes is 99.999999999% (11 nines).

---

# PART B: AWS Lambda

## 1. Overview
AWS Lambda is a **serverless, event-driven compute service** that runs code without managing servers. It scales up and down automatically with **pay-per-use pricing**.

## 2. Uses of Lambda
- **Stream processing:** real-time analytics (Kinesis Data Streams).
- **Web applications:** scalable apps that adjust to demand.
- **Mobile backends:** secure API backends.
- **IoT backends:** handle web, mobile, IoT and third-party API requests.
- **File processing:** run automatically when files are uploaded to S3.
- **Database operations:** respond to database changes.
- **Scheduled tasks:** periodic jobs using EventBridge.

## 3. How Lambda Works
1. Code is written as **Lambda functions**, the basic building blocks.
2. Security is controlled through **execution roles** and permissions.
3. **Event sources and AWS services trigger** the functions, passing event data in JSON format.
4. Lambda runs the code in execution environments using runtimes such as Node.js and Python.

The user is responsible only for the code; Lambda manages servers, operating system maintenance, capacity provisioning, scaling and logging.

## 4. Key Features
- **Configure and secure:** environment variables, versions, layers (code reuse), code signing.
- **Scale and perform:** concurrency controls, SnapStart (reduced cold start), response streaming, container images.
- **Connect and integrate:** VPC networks, file system integration, Function URLs, extensions.

---

# S3 and Lambda Together (IoT Example)
IoT device → AWS IoT Core → **Lambda** (processes data) → **S3** (stores data). An upload to S3 can also trigger a Lambda function automatically for file processing.

## Conclusion
S3 offers durable, scalable and cost-effective object storage with versioning and multiple storage classes, while Lambda offers serverless, automatically scaling compute. Together they form the storage and processing backbone of cloud-based IoT applications.
