# AWS Components

**Introduction:** Amazon Web Services (AWS) is a cloud platform that provides on-demand computing, storage, database, networking, analytics, AI and IoT services on a pay-as-you-go basis. Its components are grouped by function as follows.

## 1. Compute Services
Handle processing power and application deployment.
- **Amazon EC2 (Elastic Compute Cloud):** Virtual servers for running applications.
- **AWS Lambda:** Runs code without managing servers (serverless computing).
- **Elastic Beanstalk:** Automatically deploys and manages web applications.
- **Amazon ECS / EKS:** Container management (Docker and Kubernetes).

## 2. Storage Services
Store and retrieve data securely.
- **Amazon S3 (Simple Storage Service):** Object-based storage for files and backups.
- **Amazon EBS (Elastic Block Store):** Block storage for EC2 instances.
- **Amazon S3 Glacier:** Long-term, low-cost data archiving.
- **AWS Storage Gateway:** Connects on-premises data with AWS cloud storage.

## 3. Database Services
- **Amazon RDS:** Relational database service (MySQL, PostgreSQL, etc.).
- **Amazon DynamoDB:** Fully managed NoSQL database.
- **Amazon Redshift:** Data warehousing and analytics.
- **Amazon Aurora:** High-performance MySQL/PostgreSQL-compatible database.

## 4. Networking and Content Delivery
- **Amazon VPC (Virtual Private Cloud):** Private network within AWS.
- **Amazon Route 53:** DNS and domain registration service.
- **AWS CloudFront:** Content delivery network (CDN) for fast delivery.
- **AWS Direct Connect:** Dedicated connection between on-premises and AWS.

## 5. Security, Identity and Compliance
- **AWS IAM:** Manages users and permissions.
- **AWS KMS (Key Management Service):** Manages encryption keys.
- **AWS Shield:** Protects against DDoS attacks.
- **AWS WAF:** Filters and monitors HTTP traffic.

## 6. Analytics and Big Data
- **Amazon Kinesis:** Real-time data streaming and analytics.
- **Amazon EMR:** Big data processing using Hadoop/Spark.
- **AWS Glue:** Data integration and ETL (Extract, Transform, Load).
- **Amazon Athena:** Queries data in S3 using SQL.

## 7. Artificial Intelligence and Machine Learning
- **Amazon SageMaker:** Build, train and deploy ML models.
- **Amazon Lex:** Conversational interfaces (chatbots).
- **Amazon Polly:** Converts text to lifelike speech.
- **Amazon Rekognition:** Image and video analysis.

## 8. IoT Services
- **AWS IoT Core:** Connects IoT devices securely to the cloud (supports MQTT, MQTT over WSS, HTTPS, LoRaWAN).
- **AWS IoT Greengrass:** Runs local compute and ML on edge devices.
- **AWS IoT Analytics:** Processes and analyzes IoT data.
- **AWS IoT Device Management:** Manages and updates large IoT fleets.

## 9. Developer and Management Tools
- **AWS CloudFormation:** Infrastructure as Code (IaC).
- **Amazon CloudWatch:** Monitoring and logging of AWS resources.
- **AWS CLI / SDKs:** Command-line and software development kits.
- **AWS CodePipeline / CodeDeploy:** CI/CD tools for automated deployment.

## Key Components Relevant to IoT (Detail)

**Amazon S3**
- Object-based storage; data is kept in *buckets* (flat containers), up to 5 TB per object.
- Bucket names are globally unique, 3–63 characters, lowercase only.
- Features: versioning, MFA delete, multipart upload, lifecycle policies.
- Storage classes: Standard, Standard-IA, One Zone-IA, Intelligent Tiering, Glacier, Glacier Deep Archive.

**AWS Lambda**
- Serverless, event-driven compute with automatic scaling and pay-per-use pricing.
- Triggered by event sources (e.g., S3 uploads, IoT messages) that pass JSON event data.
- Uses: stream processing, IoT backends, file processing, scheduled tasks.

**AWS IoT Core**
- Connects devices to AWS services through a message broker using publish/subscribe.
- Accessed through the IoT Device SDKs, AWS CLI, IoT API and AWS SDKs.

## Typical Flow in an IoT Application
IoT devices → AWS IoT Core → Lambda (processing) → S3 / DynamoDB (storage) → Analytics / Dashboards

## Conclusion
AWS offers a complete set of integrated services across compute, storage, databases, networking, security, analytics, AI and IoT. This lets organizations build scalable, secure and cost-effective IoT solutions without managing physical infrastructure.
