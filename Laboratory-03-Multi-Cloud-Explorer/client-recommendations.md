# Client Recommendations

## Client A - Startup Company

**Scenario:** A startup company wants to launch a new mobile application. Their budget is limited, but they expect rapid growth within the next few years.

**Recommended Platform:** Amazon Web Services (AWS)

**Explanation:**
AWS is the best choice for a budget-conscious startup because of its pay-as-you-go pricing model, which means the company only pays for what they use. AWS also offers a Free Tier that allows startups to experiment and launch their app with minimal upfront cost. As the startup grows, AWS can easily scale resources up or down without major infrastructure changes, making it ideal for rapid growth. Additionally, AWS has a mature ecosystem of startup programs and credits that can further reduce costs.

**Services the client could use:**
1. **Amazon EC2** – Scalable virtual servers to host the mobile app backend
2. **Amazon S3** – Cost-effective storage for user data, images, and app assets
3. **AWS Lambda** – Serverless compute to run backend logic without managing servers

---

## Client B - University

**Scenario:** A university already uses Windows Server, Microsoft 365, and Active Directory. The university wants to migrate some services to the cloud.

**Recommended Platform:** Microsoft Azure

**Explanation:**
Microsoft Azure is the most appropriate choice because the university is already deeply invested in the Microsoft ecosystem. Azure natively integrates with Windows Server, Microsoft 365, and Active Directory, allowing for a seamless migration with minimal reconfiguration. The university can extend its existing Active Directory to Azure AD for hybrid identity management, and migrate on-premises Windows Server workloads to Azure Virtual Machines without compatibility issues. This reduces training costs and operational complexity since the IT staff is already familiar with Microsoft tools.

**Services the client could use:**
1. **Azure Virtual Machines** – To host migrated Windows Server workloads
2. **Microsoft Entra ID (Azure AD)** – For identity and access management
3. **Azure SQL Database** – For managed database services

---

## Client C - AI Research Company

**Scenario:** A research company develops Artificial Intelligence and Machine Learning applications that require high-performance computing.

**Recommended Platform:** Google Cloud Platform (GCP)

**Explanation:**
GCP is the strongest choice for an AI research company because Google is a pioneer in artificial intelligence and machine learning. GCP offers Vertex AI, a unified platform for building and deploying ML models, and provides access to Tensor Processing Units (TPUs) that are specifically designed for high-performance AI workloads. Google's infrastructure also supports large-scale data processing and model training more efficiently than competitors. Additionally, GCP's open-source-friendly approach and integration with popular ML frameworks like TensorFlow make it ideal for research environments.

**Services the client could use:**
1. **Vertex AI** – For building, training, and deploying machine learning models
2. **Compute Engine** – For high-performance computing with customizable VMs
3. **Cloud TPU** – For accelerated machine learning workloads

---

## Client D - Global E-Commerce Company

**Scenario:** A multinational online shopping company serves customers around the world and requires highly available infrastructure with automatic scaling.

**Recommended Platform:** Amazon Web Services (AWS)

**Explanation:**
AWS is the best fit for a global e-commerce company because of its extensive global infrastructure, with regions and edge locations spanning the entire world. AWS provides highly available services with built-in redundancy across Availability Zones, ensuring the e-commerce platform stays online even during failures. Auto Scaling and Elastic Load Balancing automatically adjust resources based on traffic demands, which is critical during peak shopping seasons. AWS also offers CloudFront CDN to deliver content quickly to customers regardless of their location.

**Services the client could use:**
1. **Amazon EC2 Auto Scaling** – Automatically adjusts compute capacity based on traffic
2. **Amazon CloudFront** – Global CDN for fast content delivery
3. **Amazon RDS** – Highly available managed database with multi-AZ deployment

---

## Multi-Cloud Decision Matrix (Checkpoint 6)

| Business Requirement | Recommended Platform | Justification |
|---|---|---|
| **Startup Company** | AWS | Pay-as-you-go pricing, Free Tier, and startup credits make it cost-effective for limited budgets. |
| **Enterprise Organization** | AWS or Azure | Both offer enterprise-grade security and compliance; choice depends on existing tech stack. |
| **Microsoft Environment** | Microsoft Azure | Native integration with Windows Server, Active Directory, and Microsoft 365. |
| **AI / Machine Learning** | Google Cloud Platform | Vertex AI, TPUs, and TensorFlow integration make it the leader in AI/ML. |
| **Kubernetes Deployment** | Google Cloud Platform | Google created Kubernetes; GKE is the most mature managed Kubernetes service. |
| **Global Web Application** | AWS | Largest global infrastructure with CloudFront CDN and multi-region availability. |
