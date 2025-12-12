# 📕 Chapter 4: Practice Questions and Exam Scenarios

> **⏱️ Estimated Time:** 2-3 hours
> **📝 Total Questions:** 75 comprehensive practice questions
> **🎯 Learning Objective:** Test your knowledge and identify weak areas

---

## 📖 Chapter Overview

Test your knowledge with these comprehensive practice questions covering all AZ-900 exam domains. All questions include detailed explanations.

**What's Included:**
- ✅ 75 practice questions across all exam domains
- 📝 Cloud Concepts questions (10 questions)
- 🏗️ Azure Architecture questions (15 questions)
- ⚙️ Management & Governance questions (20 questions)
- 🎬 Real-world scenario-based questions (30 questions)
- 💡 Detailed explanations for every answer
- 🎯 Exam tips and strategies


---

## Table of Contents
1. [Cloud Concepts Questions](#cloud-concepts-questions)
2. [**Azure** Architecture and Services Questions](#azure-architecture-and-services-questions)
3. [Management and Governance Questions](#management-and-governance-questions)
4. [Scenario-Based Questions](#scenario-based-questions)
5. [Exam Tips and Strategies](#exam-tips-and-strategies)


---

## Cloud Concepts Questions

### Question 1
Which cloud deployment model allows an organization to use resources from both an on-premises **datacenter** and a public **cloud provider**?

A: Public cloud

B: Private cloud

C: Hybrid cloud

D: Multi-cloud

<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** Hybrid cloud combines public and private clouds, allowing data and applications to move between them. This is different from multi-cloud, which uses multiple cloud providers but doesn't necessarily include on-premises infrastructure.

</details>


---

### Question 2
Your company is migrating to **Azure** and wants to convert capital expenditure (**CapEx**) to operational expenditure (**OpEx**). Which pricing model achieves this?

A: Reserved instances

B: Pay-as-you-go

C: Upfront payment

D: Enterprise agreement

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** Pay-as-you-go converts **CapEx** (large upfront hardware purchases) to **OpEx** (ongoing operational costs based on usage). This is a key benefit of cloud computing.

</details>


---

### Question 3
In the shared responsibility model, which component is ALWAYS the **cloud provider**'s responsibility, regardless of service model (**IaaS**/**PaaS**/**SaaS**)?

A: Operating system

B: Data

C: Physical **datacenter**

D: Applications

<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** The **cloud provider** always manages the physical infrastructure (**datacenter**, network, hosts). The **customer** always manages data, devices, and accounts. Other components vary by service model.

</details>


---

### Question 4
Which cloud service model provides the MOST control over the operating system and installed software?

A: Software as a Service (**SaaS**)

B: Platform as a Service (**PaaS**)

C: Infrastructure as a Service (**IaaS**)

D: Functions as a Service (FaaS)

<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** **IaaS** provides maximum control - you manage the OS, middleware, applications, and data. The provider manages only the physical infrastructure. **PaaS** abstracts the OS layer, and **SaaS** abstracts almost everything.

</details>


---

### Question 5
Which of the following is an example of Platform as a Service (**PaaS**)?

A: **Azure** Virtual Machines

B: **Azure** App Service

C: Microsoft 365

D: **Azure** Virtual Network

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** **Azure** App Service is **PaaS** - you deploy code, **Azure** manages the platform. Virtual Machines are **IaaS**. Microsoft 365 is **SaaS**. Virtual Network is **IaaS** networking.

</details>


---

### Question 6
What is a benefit of cloud computing's **elasticity**?

A: Resources never fail

B: Resources automatically scale based on demand

C: Resources are always at maximum capacity

D: Resources require manual intervention to scale

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** Elasticity is the automatic, dynamic scaling of resources in response to demand changes. It differs from **scalability**, which may require manual intervention.

</details>


---

### Question 7
Which cloud benefit ensures that your applications can recover quickly from failures?

A: Scalability

B: Reliability

C: Predictability

D: Manageability

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** Reliability is the ability to recover from failures and continue functioning. It's enabled through redundancy, failover, and **Azure**'s global infrastructure.

</details>


---

### Question 8
In the shared responsibility model for **SaaS**, who is responsible for managing user accounts and access?

A: Cloud provider only

B: Customer only

C: Shared between provider and **customer**

D: Third-party vendor

<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** In **SaaS**, the provider manages the application infrastructure, but the **customer** manages user identity, accounts, and access permissions (like who can access what in Microsoft 365).

</details>


---

### Question 9
Which characteristic distinguishes a private cloud from a public cloud?

A: Private cloud is free

B: Private cloud is dedicated to one organization

C: Private cloud doesn't require internet

D: Private cloud has no **scalability**

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** Private cloud is single-tenant, dedicated exclusively to one organization. It can be on-premises or hosted. Public cloud is multi-tenant with shared resources.

</details>


---

### Question 10
What does "consumption-based model" mean in cloud computing?

A: Pay fixed monthly fee regardless of usage

B: Pay upfront for all resources

C: Pay only for resources you use

D: Free access to all cloud services

<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** Consumption-based (pay-as-you-go) means you're charged based on actual usage. Stop using resources, stop paying. This converts **CapEx** to **OpEx**.

</details>


---

## **Azure** Architecture and Services Questions

### Question 11
How many availability zones are in an availability **zone**-enabled **Azure** **region**?

A: 1

B: 2

C: 3 or more

D: Unlimited

<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** Availability **zone**-enabled regions have a minimum of 3 physically separate datacenters (zones). Not all regions support availability zones.

</details>


---

### Question 12
What is the **SLA** for virtual machines deployed across two or more availability zones?

A: 99.9%

B: 99.95%

C: 99.99%

D: 99.999%

<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** **VMs** across availability zones get 99.99% **SLA** (highest for **VMs**). Single **VM** with Premium SSD = 99.9%. **VMs** in availability set = 99.95%.

</details>


---

### Question 13
Which storage redundancy option replicates data to a secondary **region** for disaster recovery?

A: Locally Redundant Storage (LRS)

B: Zone-Redundant Storage (ZRS)

C: Geo-Redundant Storage (GRS)

D: Standard Storage

<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** GRS replicates data to a paired **region** hundreds of miles away (6 copies total: 3 local + 3 remote). LRS and ZRS keep data within one **region**.

</details>


---

### Question 14
Your company needs to run containers in **Azure** with full Kubernetes orchestration capabilities. Which service should you use?

A: **Azure** Container Instances (ACI)

B: **Azure** Kubernetes Service (AKS)

C: **Azure** Virtual Machines

D: **Azure** App Service

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** AKS is managed Kubernetes for container orchestration. ACI is for simple containers without orchestration. **VMs** and App Service aren't container-focused.

</details>


---

### Question 15
Which **Azure** service provides event-driven, serverless compute where you pay only when your code executes?

A: **Azure** Virtual Machines

B: **Azure** App Service

C: **Azure** Functions

D: **Azure** Container Instances

<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** **Azure** Functions is serverless and event-driven. You pay per execution, not for idle time. It's perfect for short-lived, event-driven tasks.

</details>


---

### Question 16
What is the primary difference between **Azure** **VPN Gateway** and **Azure** **ExpressRoute**?

A: **VPN Gateway** is faster

B: **ExpressRoute** uses a private connection that doesn't go over the internet

C: **VPN Gateway** is more expensive

D: **ExpressRoute** only works with Windows

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** **ExpressRoute** is a private, dedicated connection. **VPN Gateway** sends encrypted traffic over the public internet. **ExpressRoute** offers higher speeds, lower latency, but costs more.

</details>


---

### Question 17
Which load balancing service operates at Layer 7 (application layer) and provides Web Application Firewall capabilities?

A: **Azure** Load Balancer

B: **Azure** Application Gateway

C: **Azure** Traffic Manager

D: **Azure** Front Door

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** Application Gateway operates at Layer 7 (HTTP/HTTPS) and includes WAF. Load Balancer operates at Layer 4 (TCP/UDP). Both Front Door and Application Gateway have WAF, but Application Gateway is the regional option.

</details>


---

### Question 18
Which storage access tier is best for data that is rarely accessed and stored for at least 180 days?

A: Hot

B: Cool

C: Cold

D: Archive

<details>
<summary>✅ Show Answer</summary>

**Answer:** D

💡 **Explanation:** Archive tier is for rarely accessed data stored 180+ days, with lowest storage cost but hours of retrieval latency. Hot = frequent access, Cool = 30+ days, Cold = 90+ days.

</details>


---

### Question 19
What is the maximum number of resource groups a single **Azure** resource can be in?

A: 0 (resources don't need resource groups)

B: 1

C: Multiple

D: Unlimited

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** Each resource must be in exactly one resource group. Resources can interact across groups, but each resource belongs to only one group at a time.

</details>


---

### Question 20
Which **Azure** database service is best for a globally distributed application requiring single-digit millisecond latency and multi-model support?

A: **Azure** **SQL Database**

B: **Azure** **Cosmos DB**

C: **Azure** Database for MySQL

D: **Azure** Table Storage

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** **Cosmos DB** is designed for global distribution, low latency (single-digit milliseconds), and supports multiple APIs (SQL, MongoDB, Cassandra, etc.). It's ideal for mission-critical global applications.

</details>


---

### Question 21
What happens to resources in a resource group when you delete the resource group?

A: Resources are moved to a default resource group

B: Resources are archived for 30 days

C: All resources in the group are deleted

D: Resources remain but are unmanaged

<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** Deleting a resource group deletes ALL resources within it. This is permanent and immediate. Be very careful with this operation.

</details>


---

### Question 22
Which **Azure** Active Directory feature allows users to sign in once and access multiple applications?

A: Multi-Factor Authentication (**MFA**)

B: Single Sign-On (**SSO**)

C: Conditional Access

D: Passwordless authentication

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** **SSO** allows one identity to access multiple applications without repeated login prompts. **MFA** adds security, but **SSO** improves convenience.

</details>


---

### Question 23
Your organization needs to migrate 200 TB of data to **Azure** but has limited internet bandwidth. Which service should you use?

A: AzCopy

B: **Azure** Storage Explorer

C: **Azure** Data Box

D: **Azure** File Sync

<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** Data Box is a physical device shipped to you for massive offline data transfers when network isn't practical. Microsoft ships it, you load data, ship back, they upload to **Azure**.

</details>


---

### Question 24
Which authentication method provides the highest security by eliminating passwords entirely?

A: Single Sign-On

B: Multi-Factor Authentication

C: Passwordless authentication

D: Basic authentication

<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** Passwordless (Windows Hello, FIDO2 keys, Authenticator app) eliminates password vulnerabilities entirely. **MFA** is more secure than passwords alone, but passwordless is best.

</details>


---

### Question 25
What is the purpose of **Azure** **region** pairs?

A: Load balancing traffic between regions

B: Disaster recovery and business continuity

C: Reducing costs

D: Improving application performance

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** Region pairs enable disaster recovery with replication to a paired **region** 300+ miles away. Only one **region** in a pair is updated at a time during planned maintenance.

</details>


---

## Management and Governance Questions

### Question 26
Which tool should you use to estimate the monthly cost of **Azure** services BEFORE deploying them?

A: **Azure** Cost Management

B: **Azure** Pricing Calculator

C: TCO Calculator

D: **Azure** Advisor

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** Pricing Calculator estimates costs before deployment. Cost Management tracks actual spending after deployment. TCO compares on-premises vs **Azure**.

</details>


---

### Question 27
Your company wants to compare the total cost of running infrastructure on-premises versus migrating to **Azure**. Which tool should you use?

A: Pricing Calculator

B: TCO Calculator

C: **Azure** Advisor

D: Cost Management

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** TCO (Total Cost of Ownership) Calculator compares on-premises costs (hardware, power, facilities, labor) with **Azure** costs to justify migration.

</details>


---

### Question 28
Which **Azure** feature prevents users from accidentally deleting critical resources?

A: **Azure** Policy

B: **RBAC**

C: Resource locks

D: Management groups

<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** Resource locks (CanNotDelete or ReadOnly) prevent deletion or modification even for users with permissions. Locks override **RBAC**.

</details>


---

### Question 29
You need to ensure all storage accounts created in your **subscription** have encryption enabled. What should you use?

A: **Azure** Blueprints

B: **Azure** Policy

C: **RBAC**

D: Resource locks

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** **Azure** Policy enforces rules and compliance on resource configurations. It can prevent creation of non-compliant resources or audit existing ones.

</details>


---

### Question 30
What is the primary difference between **Azure** Policy and **RBAC**?

A: Policy is for cost management, **RBAC** is for security

B: Policy controls what configurations are allowed, **RBAC** controls who can perform actions

C: They are the same thing

D: Policy is older than **RBAC**

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** **RBAC** = WHO can do WHAT (authorization). Policy = WHAT resource configurations are allowed (compliance). They work together but serve different purposes.

</details>


---

### Question 31
Which type of resource lock allows users to read and modify a resource but not delete it?

A: ReadOnly

B: CanNotDelete

C: DoNotModify

D: Protected

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** CanNotDelete allows read and modify operations but prevents deletion. ReadOnly prevents all modifications and deletions.

</details>


---

### Question 32
Which **Azure** service provides personalized recommendations to improve security, performance, and reduce costs?

A: **Azure** Monitor

B: Service Health

C: **Azure** Advisor

D: Application Insights

<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** Advisor provides free recommendations across 5 categories: Reliability, Security, Performance, Cost, and Operational Excellence. It's like a personalized cloud consultant.

</details>


---

### Question 33
Which command-line tool uses cmdlets in the format `Verb-AzNoun`?

A: **Azure** CLI

B: **Azure** PowerShell

C: Bash

D: ARM

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** PowerShell uses `Verb-AzNoun` format (e.g., `Get-AzVM`). **Azure** CLI uses `az group command` format (e.g., `az vm list`).

</details>


---

### Question 34
What is the primary purpose of **Azure** Resource Manager (ARM)?

A: Monitor resources

B: Provide a consistent management layer for all **Azure** operations

C: Store data

D: Control costs

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** ARM is the deployment and management layer that all tools (Portal, CLI, PowerShell, SDKs) use. It provides consistent management APIs and enables features like **RBAC**, tags, and templates.

</details>


---

### Question 35
Which **Azure** service extends **Azure** management capabilities to on-premises and multi-cloud environments?

A: **Azure** **VPN Gateway**

B: **Azure** **ExpressRoute**

C: **Azure** Arc

D: **Azure** Migrate

<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** **Azure** Arc allows you to manage on-premises servers, Kubernetes clusters, and resources in other clouds using **Azure** tools, policies, and **RBAC**.

</details>


---

### Question 36
What is the main benefit of using ARM templates?

A: Reduce costs

B: Define infrastructure as code for consistent deployments

C: Monitor applications

D: Improve security

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** ARM templates (JSON) enable Infrastructure as Code - consistent, repeatable deployments, version control, and automation. They reduce errors and ensure identical environments.

</details>


---

### Question 37
Which **Azure** Monitor component is specifically designed for monitoring web application performance and usage?

A: Metrics

B: Logs

C: Application Insights

D: Alerts

<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** Application Insights is the APM (Application Performance Management) component for monitoring live web applications, detecting anomalies, and analyzing usage.

</details>


---

### Question 38
What query language is used in **Azure** Log Analytics?

A: SQL

B: PowerShell

C: Kusto Query Language (KQL)

D: Python

<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** Log Analytics uses KQL (Kusto Query Language) to query and analyze log data from various sources.

</details>


---

### Question 39
Which **Azure** service provides information about planned maintenance and service issues affecting YOUR specific resources?

A: **Azure** Status

B: Service Health

C: **Azure** Monitor

D: **Azure** Advisor

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** Service Health provides personalized views of health for services and regions you use. **Azure** Status shows global service health (not personalized).

</details>


---

### Question 40
What is a composite **SLA**?

A: The average of all service SLAs

B: The product of individual service SLAs when using multiple services

C: The highest **SLA** among services used

D: The lowest **SLA** among services used

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** Composite **SLA** = SLA₁ × SLA₂ × SLA₃. For example: 99.95% × 99.99% = 99.94%. More dependencies generally mean lower overall **SLA**.

</details>


---

### Question 41
Which support plan is the minimum tier that provides 24/7 technical support via phone?

A: Basic

B: Developer

C: Standard

D: Professional Direct

<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** Standard ($100/month) provides 24/7 technical support via email and phone. Developer only offers business hours email support. Basic has no technical support.

</details>


---

### Question 42
What is the approximate downtime per year for a 99.9% **SLA**?

A: 52 minutes

B: 8.7 hours

C: 4.4 hours

D: 3.65 days

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** 99.9% uptime = 0.1% downtime = ~8.76 hours per year, or ~43.2 minutes per month.

</details>


---

### Question 43
Which **Azure** feature allows you to organize resources and track costs by department or project?

A: Resource groups

B: Tags

C: Subscriptions

D: Management groups

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** Tags are name-value pairs for organizing resources and tracking costs. They enable chargeback/showback by department, project, environment, etc.

</details>


---

### Question 44
What is the purpose of **Azure** Blueprints?

A: Design network diagrams

B: Package ARM templates, policies, and **RBAC** assignments for repeatable deployments

C: Monitor resource health

D: Estimate costs

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** Blueprints bundle together resource templates, policies, role assignments, and resource groups for rapid, compliant environment deployment with versioning.

</details>


---

### Question 45
Which **Azure** service provides unified data governance across on-premises, multi-cloud, and **SaaS** data?

A: **Azure** Policy

B: Microsoft Purview

C: **Azure** Monitor

D: **Azure** Advisor

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** Microsoft Purview provides data discovery, classification, lineage, and governance across hybrid and multi-cloud environments.

</details>


---

## Scenario-Based Questions

### Scenario 1: High Availability Web Application

**Scenario**: Your company is deploying a mission-critical web application that must achieve maximum uptime and handle variable traffic loads.

**Question 46**: Which compute option provides automatic scaling and **high availability** without managing **VMs**?

A: **Azure** Virtual Machines with manual scaling

B: **Azure** App Service with autoscale

C: On-premises servers

D: Single **Azure** **VM**

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** App Service (**PaaS**) provides automatic scaling, **high availability**, and no **VM** management. It's perfect for web apps with variable traffic.

</details>


---

**Question 47**: To maximize uptime, you deploy the application across multiple **Azure** datacenters in the same **region**. What feature are you using?

A: Availability Set

B: Availability Zones

C: Region Pairs

D: Load Balancer



<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** Availability zones are physically separate datacenters within a **region**, providing the highest **SLA** (99.99%) for protection against **datacenter** failures.

</details>


---

**Question 48**: The application stores user-uploaded images. Which storage service should you use?

A: **Azure** **SQL Database**

B: **Azure** **Blob Storage**

C: **Azure** Queue Storage

D: **Azure** Table Storage



<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** **Blob Storage** is object storage designed for files, images, videos, and unstructured data. It's scalable and cost-effective for this use case.

</details>



---

### Scenario 2: Cost Optimization

**Scenario**: Your company has deployed 100 **VMs** in **Azure** for development and testing. They run 8 hours/day on weekdays only. Management wants to reduce costs.

**Question 49**: What should you implement to stop incurring compute charges when **VMs** aren't needed?

A: Stop the **VMs**

B: Deallocate the **VMs**

C: Delete the **VMs** daily

D: Reduce **VM** sizes

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** Deallocating **VMs** releases compute resources and stops compute charges (storage still charged). Simply stopping **VMs** continues charges. Auto-shutdown policies can automate this.

</details>


---

**Question 50**: Which pricing option would provide the greatest discount for production **VMs** that run 24/7?

A: Pay-as-you-go

B: Spot **VMs**

C: Reserved Instances (1 or 3 year)

D: Free tier



<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** Reserved instances save up to 72% for committed workloads running continuously. Spot **VMs** are cheaper but can be evicted. Pay-as-you-go has no discount.

</details>


---

**Question 51**: Which tool should the finance team use to track actual spending and set budget alerts?

A: Pricing Calculator

B: **Azure** Cost Management

C: TCO Calculator

D: **Azure** Advisor



<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** Cost Management tracks actual spending, provides cost analysis, sets budgets with alerts, and offers optimization recommendations.

</details>



---

### Scenario 3: Hybrid Cloud Deployment

**Scenario**: A financial services company must keep sensitive **customer** data on-premises due to regulations but wants to use **Azure** for web front-ends and analytics.

**Question 52**: Which cloud deployment model should they use?

A: Public cloud

B: Private cloud

C: Hybrid cloud

D: Community cloud

<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** Hybrid cloud allows sensitive data to remain on-premises while leveraging public cloud for other workloads, meeting both compliance and cloud benefits.

</details>


---

**Question 53**: Which connectivity option provides a private, dedicated connection between on-premises and **Azure** (not over internet)?

A: Site-to-Site VPN

B: Point-to-Site VPN

C: **Azure** **ExpressRoute**

D: Public internet



<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** **ExpressRoute** provides a private, dedicated connection that doesn't traverse the internet, offering better security, performance, and reliability for sensitive data.

</details>


---

**Question 54**: How can they manage on-premises servers using **Azure** governance tools and policies?

A: **VPN Gateway**

B: **ExpressRoute**

C: **Azure** Arc

D: **Azure** Migrate



<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** **Azure** Arc extends **Azure** management, governance, and policies to on-premises servers, allowing unified management across hybrid environments.

</details>



---

### Scenario 4: Global E-Commerce Platform

**Scenario**: An e-commerce company is deploying a global application that needs low-latency access to product catalog data from anywhere in the world.

**Question 55**: Which database service should they use for the product catalog?

A: **Azure** **SQL Database** (single **region**)

B: **Azure** **Cosmos DB** with geo-replication

C: **Azure** Database for MySQL

D: **Azure** Table Storage

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** **Cosmos DB** provides turnkey global distribution, single-digit millisecond latency worldwide, and 99.999% availability **SLA** (multi-**region**) - perfect for global applications.

</details>


---

**Question 56**: To serve static content (images, CSS, JavaScript) with low latency globally, what should they use?

A: **Azure** **Blob Storage** only

B: **Azure** Front Door with CDN

C: **Azure** **VPN Gateway**

D: **Azure** **ExpressRoute**



<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** **Azure** Front Door is a global load balancer with integrated CDN, providing fast content delivery worldwide with caching at edge locations.

</details>


---

**Question 57**: They need to process order transactions that may spike during sales events. Which compute service automatically scales and charges only for actual execution time?

A: **Azure** Virtual Machines

B: **Azure** App Service

C: **Azure** Functions

D: **Azure** Kubernetes Service



<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** **Azure** Functions is serverless and event-driven, perfect for variable workloads. It automatically scales and you pay only per execution, ideal for spiky order processing.

</details>



---

### Scenario 5: Security and Compliance

**Scenario**: A healthcare organization is migrating patient records to **Azure** and must comply with HIPAA regulations.

**Question 58**: Which should they implement to require multi-factor authentication for users accessing patient data from outside the corporate network?

A: **Azure** Policy

B: Conditional Access

C: **RBAC**

D: Resource Locks

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** Conditional Access creates if/then policies based on signals (location, device, user, risk). It can enforce **MFA** when accessing from untrusted locations.

</details>


---

**Question 59**: To ensure patient data is protected against regional disasters, which storage redundancy should they use?

A: LRS (Locally Redundant Storage)

B: ZRS (Zone-Redundant Storage)

C: GRS (Geo-Redundant Storage)

D: Standard Storage



<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** GRS replicates data to a paired **region** hundreds of miles away, protecting against regional disasters. This ensures business continuity and data protection.

</details>


---

**Question 60**: They need to prevent any accidental deletion of storage accounts containing patient records. What should they implement?

A: **Azure** Policy

B: **RBAC**

C: CanNotDelete resource lock

D: ReadOnly resource lock



<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** CanNotDelete lock prevents deletion while still allowing reads and modifications. This protects critical resources from accidental deletion regardless of user permissions.

</details>



---

### Scenario 6: DevOps and Automation

**Scenario**: A software company wants to automate deployment of identical development, testing, and production environments.

**Question 61**: What should they use to define infrastructure as code for repeatable deployments?

A: **Azure** Portal

B: ARM Templates

C: **Azure** CLI scripts only

D: Manual deployment

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** ARM Templates (JSON) define infrastructure as code, ensuring consistent, repeatable deployments across all environments. They can be version-controlled and automated.

</details>


---

**Question 62**: They want to ensure all resources deployed have required tags (Environment, Owner, CostCenter). What should they use?

A: **Azure** Blueprints

B: **Azure** Policy

C: **RBAC**

D: Resource Locks



<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** **Azure** Policy can require specific tags on resources. It can deny deployment of resources without required tags or automatically append tags.

</details>


---

**Question 63**: To package ARM templates, policies, and role assignments together for deploying compliant environments, what should they use?

A: Resource Groups

B: Management Groups

C: **Azure** Blueprints

D: Subscriptions



<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** Blueprints package ARM templates, policies, and **RBAC** assignments together for rapid deployment of fully compliant environments with versioning and tracking.

</details>



---

### Scenario 7: Migration Planning

**Scenario**: A company with 200 on-premises servers is considering migrating to **Azure**.

**Question 64**: Which tool should they use to justify the migration by comparing on-premises costs with **Azure** costs?

A: **Azure** Pricing Calculator

B: TCO Calculator

C: **Azure** Cost Management

D: **Azure** Migrate

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** TCO Calculator compares total on-premises costs (hardware, power, cooling, facilities, labor) with **Azure** costs to build a business case for migration.

</details>


---

**Question 65**: For a gradual migration where some servers move immediately and others remain on-premises temporarily, which deployment model applies?

A: Public cloud

B: Private cloud

C: Hybrid cloud

D: Multi-cloud



<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** Hybrid cloud allows gradual migration with some workloads in **Azure** and others on-premises, connected together, providing flexibility during transition.

</details>


---

**Question 66**: They have 500 TB of historical data to migrate. Network bandwidth is limited. Which service should they use?

A: AzCopy

B: **Azure** Data Box

C: **Azure** Storage Explorer

D: Manual upload



<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** **Azure** Data Box is a physical device for massive offline data transfers when network transfer isn't practical. Microsoft ships it, you load data, ship back, they upload.

</details>



---

### Scenario 8: Monitoring and Troubleshooting

**Scenario**: A web application in **Azure** is experiencing performance issues and occasional errors.

**Question 67**: Which service provides detailed application performance monitoring, request tracking, and exception detection?

A: **Azure** Monitor Metrics

B: Application Insights

C: Service Health

D: **Azure** Advisor

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** Application Insights is the APM tool for deep application monitoring, tracking requests, exceptions, dependencies, and performance with built-in analytics.

</details>


---

**Question 68**: To query application logs and analyze error patterns, which tool should they use?

A: **Azure** Portal dashboards

B: Log Analytics with KQL

C: **Azure** Advisor

D: Service Health



<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** Log Analytics allows querying logs using KQL (Kusto Query Language) to analyze patterns, troubleshoot issues, and create custom visualizations.

</details>


---

**Question 69**: They want recommendations for improving performance and reducing costs. Which service provides this?

A: **Azure** Monitor

B: Service Health

C: **Azure** Advisor

D: Application Insights



<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** **Azure** Advisor provides personalized recommendations across 5 categories including Performance and Cost, analyzing your resources and suggesting improvements.

</details>



---

### Scenario 9: Data Protection

**Scenario**: A company needs to ensure business continuity and disaster recovery for critical applications.

**Question 70**: To protect against an entire **Azure** **region** becoming unavailable, what should they implement?

A: Availability Set

B: Availability Zones

C: Region Pairs with geo-replication

D: Single **VM** backups

<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** Region pairs provide disaster recovery across geographically distant regions. Replicating to a paired **region** protects against regional failures.

</details>


---

**Question 71**: For virtual machine backups with simple point-in-time recovery, which service should they use?

A: **Azure** Backup

B: **Azure** Site Recovery

C: Manual snapshots only

D: **Azure** Storage replication



<details>
<summary>✅ Show Answer</summary>

**Answer:** A

💡 **Explanation:** **Azure** Backup provides centralized backup management with point-in-time recovery for **VMs**, databases, and files. It's purpose-built for backup and restore scenarios.

</details>



---

### Scenario 10: Identity and Access

**Scenario**: A multinational corporation needs to manage access for 10,000 employees across multiple **Azure** subscriptions.

**Question 72**: To organize multiple subscriptions and apply policies across all of them, what should they use?

A: Resource Groups

B: Management Groups

C: Tags

D: Multiple administrators

<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** Management Groups organize multiple subscriptions hierarchically, allowing policies and access control to be applied at scale across all subscriptions.

</details>


---

**Question 73**: To control WHO can perform actions on resources, what should they use?

A: **Azure** Policy

B: Role-Based Access Control (**RBAC**)

C: Resource Locks

D: Network Security Groups



<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** **RBAC** controls authorization - who can perform what actions on which resources. It's the primary access control mechanism in **Azure**.

</details>


---

**Question 74**: To ensure users must verify their identity with a phone before accessing **Azure** Portal, what should they enable?

A: Single Sign-On

B: Multi-Factor Authentication (**MFA**)

C: Conditional Access

D: Passwordless authentication



<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** **MFA** requires two or more verification factors (something you know + something you have/are). It significantly improves security for user accounts.

</details>


---

**Question 75**: They want to allow partner companies to collaborate on **Azure** projects using their own corporate credentials. Which **Azure** AD feature should they use?

A: **Azure** AD B2C

B: **Azure** AD B2B

C: Conditional Access

D: **RBAC**


<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** **Azure** AD B2B (Business-to-Business) allows external partners to use their own credentials to access your resources without managing separate accounts for them.

</details>

---


## Exam Tips and Strategies

### Before the Exam

**1. Study All Domains Thoroughly**
- Cloud Concepts (25-30%)
- **Azure** Architecture and Services (35-40%) - largest section
- Management and Governance (30-35%)

**2. Hands-On Practice**
- Create free **Azure** account ($200 credit)
- Deploy **VMs**, storage accounts, web apps
- Explore **Azure** Portal, CLI, PowerShell
- Practice cost estimation with calculators

**3. Focus on High-Frequency Topics**
- **IaaS** vs **PaaS** vs **SaaS** examples
- Shared responsibility model
- Storage redundancy options
- Virtual network concepts
- Cost optimization strategies
- **RBAC**, policies, and locks
- **SLA** calculations
- Support plans

**4. Memorize Key Facts**
- **SLA** percentages and downtime
- Storage redundancy (LRS, ZRS, GRS, GZRS)
- Service model responsibilities
- Support plan features and costs
- Availability **zone** minimum (3)
- Region pair distance (300+ miles)

### During the Exam

**1. Time Management**
- 60 minutes for 40-60 questions
- About 1-1.5 minutes per question
- Don't spend too long on any question
- Mark difficult questions for review

**2. Read Carefully**
- Look for keywords:
  - "Least cost" vs "Highest availability"
  - "Minimum administrative effort"
  - "Must" vs "Should"
  - "Prevent" vs "Alert"
- Understand what's being asked before looking at answers

**3. Elimination Strategy**
- Cross out obviously wrong answers
- Choose from remaining options
- If unsure, make educated guess (no penalty for wrong answers)

**4. Question Types**

**Multiple Choice**:
- One correct answer
- Eliminate clearly wrong options first

**Multiple Select**:
- Carefully note how many to select
- Select exactly that number

**Drag and Drop**:
- Match items correctly
- Often involves sequencing or categorization

**Case Studies**:
- Read scenario carefully
- Multiple questions based on same scenario
- Take notes on requirements

**5. Common Traps to Avoid**
- Don't confuse similar services (**VPN Gateway** vs **ExpressRoute**)
- Watch for "NOT" or "EXCEPT" in questions
- Distinguish between cost estimation tools (Pricing vs TCO)
- Know the difference between monitoring services

**6. When Uncertain**
- Trust your first instinct (usually correct)
- Don't overthink fundamentals questions
- Remember: this is entry-level certification
- Answers are straightforward, not tricky

### Answer Strategies by Topic

**Cloud Concepts**:
- Know service models: **IaaS** (most control), **PaaS** (balance), **SaaS** (least control)
- Shared responsibility: Provider owns physical, **customer** owns data
- Deployment models: Match to scenario requirements

**Architecture & Services**:
- Choose services based on requirements:
  - Full control needed → **IaaS** (**VMs**)
  - Focus on code → **PaaS** (App Service, Functions)
  - Ready to use → **SaaS**
- Storage redundancy: More redundancy = higher cost, higher availability
- Networking: VPN = internet, **ExpressRoute** = private

**Management & Governance**:
- Cost questions: Match tool to purpose (estimate vs actual vs compare)
- Governance: Policy = WHAT, **RBAC** = WHO, Locks = PREVENT
- Monitoring: Match service to need (recommendations, health, metrics, logs)

### Final Checklist

**Day Before Exam**:
- Review this practice questions chapter
- Review chapter summaries
- Review glossary for unfamiliar terms
- Get good sleep
- Prepare ID and confirmation

**Exam Day**:
- Arrive early (or log in early for online)
- Read tutorial (doesn't count against time)
- Use all 60 minutes (review marked questions)
- Don't leave questions unanswered
- Stay calm and confident

### After These Practice Questions

**Score Yourself**:
- 90-100%: Excellent! Ready for exam
- 75-89%: Good! Review missed topics
- 60-74%: More study needed, focus on weak areas
- Below 60%: Review all chapters again

**Next Steps**:
1. Review questions you got wrong
2. Read explanations for all questions
3. Revisit relevant chapter sections
4. Take official Microsoft practice assessment
5. Schedule your exam when consistently scoring 85%+


---

## Summary

You've completed 75 comprehensive practice questions covering:
- All three exam domains
- Scenario-based questions
- Common exam traps
- Strategic approaches

**Key Takeaways**:
- Understand concepts, don't just memorize
- Know when to use each service
- Practice with **Azure** Portal (hands-on)
- Focus on frequently tested topics
- Read questions carefully for keywords

**Final Preparation**:
Review [Chapter 5: Glossary and Quick Reference](05-glossary.md) for terminology and quick reference materials before your exam.

**You're well-prepared! Good luck on your AZ-900 exam!**
