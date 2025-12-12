# 📘 Chapter 1: Cloud Concepts

> **📊 Exam Weight:** 25-30% of total exam
> **⏱️ Estimated Time:** 2-3 hours
> **📝 Practice Questions:** 10 questions at end of chapter
> **🎯 Learning Objective:** Master fundamental cloud computing concepts

---

## 📖 Chapter Overview

This chapter covers fundamental cloud computing concepts that form the foundation of the AZ-900 exam. Understanding these concepts is critical for success.

**What You'll Learn:**
- ☁️ Core cloud computing principles and benefits
- 🔒 Shared responsibility between provider and customer
- 🏗️ Service models: IaaS, PaaS, SaaS
- 🌍 Deployment models: Public, Private, Hybrid
- 💰 Consumption-based pricing model
- 🚀 Cloud advantages and use cases


---

## Table of Contents
1. [What is Cloud Computing](#what-is-cloud-computing)
2. [Shared Responsibility Model](#shared-responsibility-model)
3. [Cloud Service Models](#cloud-service-models)
4. [Cloud Deployment Models](#cloud-deployment-models)
5. [Consumption-Based Model](#consumption-based-model)
6. [Benefits of Cloud Computing](#benefits-of-cloud-computing)
7. [Chapter Summary](#chapter-summary)
8. [Practice Questions](#practice-questions)


---

## What is Cloud Computing

### Definition
**Cloud computing** is the delivery of computing services over the internet (the cloud), including:
- Compute power (virtual machines, containers)
- Storage (files, databases)
- Networking (virtual networks, load balancers)
- Analytics and intelligence
- Software applications

### Key Characteristics
1. **On-demand self-service**: Provision resources without human interaction
2. **Broad network access**: Available over the network via standard devices
3. **Resource pooling**: Provider resources serve multiple customers
4. **Rapid elasticity**: Scale up or down quickly based on demand
5. **Measured service**: Pay only for what you use

### Why Use Cloud Computing?
- **No upfront infrastructure costs**: No need to buy servers or build datacenters
- **Global reach**: Deploy applications worldwide in minutes
- **Flexibility**: Scale resources up or down based on demand
- **Reliability**: Built-in backup, disaster recovery, and redundancy
- **Innovation**: Access to latest technologies (AI, IoT, analytics)

> **💡 EXAM TIP:** Understand that cloud computing eliminates the need for upfront capital expenditure (**CapEx**) and converts it to operational expenditure (**OpEx**).


---

## Shared Responsibility Model

The **shared responsibility model** defines which security and operational tasks are handled by the **cloud provider** versus the **customer**.

### Responsibility Distribution

#### Always Customer Responsibility (You manage):
- **Information and data**
- **Devices** (mobile, PCs, tablets)
- **Accounts and identities**

#### Always Provider Responsibility (Microsoft manages):
- **Physical datacenter**
- **Physical network**
- **Physical hosts**

#### Varies by Service Type:
- **Operating system**
- **Network controls**
- **Applications**
- **Identity and directory infrastructure**

### Shared Responsibility by Service Model

```
┌─────────────────────────────────────────────────────────────┐
│                    Responsibility Matrix                     │
├─────────────────────────┬──────────┬──────────┬─────────────┤
│ Component               │   **SaaS**   │   **PaaS**   │    **IaaS**     │
├─────────────────────────┼──────────┼──────────┼─────────────┤
│ Information & Data      │ Customer │ Customer │  Customer   │
│ Devices                 │ Customer │ Customer │  Customer   │
│ Accounts & Identities   │ Customer │ Customer │  Customer   │
│ Identity Infrastructure │ Shared   │ Shared   │  Customer   │
│ Applications            │ Provider │ Shared   │  Customer   │
│ Network Controls        │ Provider │ Shared   │  Customer   │
│ Operating System        │ Provider │ Provider │  Customer   │
│ Physical Hosts          │ Provider │ Provider │  Provider   │
│ Physical Network        │ Provider │ Provider │  Provider   │
│ Physical Datacenter     │ Provider │ Provider │  Provider   │
└─────────────────────────┴──────────┴──────────┴─────────────┘
```

### 🎯 Key Takeaways

> **💡 QUICK RECAP:**
> 
- **SaaS**: Provider manages most; **customer** manages data and access
- **PaaS**: Shared responsibilities for apps and network
- **IaaS**: Customer manages everything except physical infrastructure

> **💡 EXAM TIP:** Memorize what the **customer** ALWAYS owns: Data, Devices, Accounts. And what Microsoft ALWAYS owns: Physical **datacenter**, network, and hosts.


---

## Cloud Service Models

Understanding the differences between **IaaS**, **PaaS**, and **SaaS** is crucial for the exam.

### Infrastructure as a Service (**IaaS**)

> **📖 Definition:** Rent IT infrastructure (servers, **VMs**, storage, networks) from a **cloud provider**.

**Customer Manages**:
- Operating systems
- Middleware
- Runtime
- Applications
- Data

**Provider Manages**:
- Virtualization
- Servers
- Storage
- Networking

****Azure** **IaaS** Examples**:
- ****Azure** Virtual Machines**: Windows or Linux **VMs**
- ****Azure** Virtual Network**: Isolated networks in the cloud
- ****Azure** Storage**: Blob, file, and disk storage

**📋 Common Use Cases:**
- Migrating on-premises workloads ("lift and shift")
- Testing and development environments
- Custom applications requiring specific OS configurations
- High-performance computing

**Analogy**: Renting a car - you control where to drive, but the rental company maintains the vehicle.

### Platform as a Service (**PaaS**)

> **📖 Definition:** Provides a complete development and deployment environment in the cloud.

**Customer Manages**:
- Applications
- Data

**Provider Manages**:
- Operating systems
- Middleware
- Runtime
- Virtualization
- Servers
- Storage
- Networking

****Azure** **PaaS** Examples**:
- ****Azure** App Service**: Host web apps, REST APIs, mobile backends
- ****Azure** SQL Database**: Managed relational database
- ****Azure** Functions**: Serverless compute
- ****Azure** Cognitive Services**: Pre-built AI models

**📋 Common Use Cases:**
- Developing cloud-native applications
- Rapid application development and deployment
- Focus on code, not infrastructure management
- Built-in **scalability** and **high availability**

**Analogy**: Renting a fully furnished apartment - you bring your belongings, landlord manages building maintenance.

### Software as a Service (**SaaS**)

> **📖 Definition:** Complete software solution delivered over the internet on a **subscription** basis.

**Customer Manages**:
- Data stored in the application
- User access and permissions

**Provider Manages**:
- Everything else (application, runtime, OS, infrastructure)

****Azure**/Microsoft **SaaS** Examples**:
- **Microsoft 365**: Office apps (Word, Excel, Outlook)
- **Microsoft Teams**: Collaboration and communication
- **Dynamics 365**: Business applications (CRM, ERP)
- **OneDrive**: Cloud file storage and sharing

**📋 Common Use Cases:**
- Email and collaboration tools
- CRM and ERP systems
- Productivity applications
- No IT management required

**Analogy**: Using a taxi/Uber - you just use the service, driver handles everything.

### Comparison Table

| Feature | **IaaS** | **PaaS** | **SaaS** |
|---------|------|------|------|
| **Control** | Maximum | Medium | Minimum |
| **Flexibility** | Highest | Medium | Lowest |
| **Management Effort** | Highest | Medium | Lowest |
| **Technical Knowledge Required** | High | Medium | Low |
| **Time to Deploy** | Longer | Medium | Fastest |
| **Cost Predictability** | Variable | More predictable | Most predictable |
| **Example Use** | Custom apps, full control | App development | Email, collaboration |

> **💡 EXAM TIP:** Remember the progression - **IaaS** gives you the most control but requires the most management. **SaaS** is fully managed but offers the least control. **PaaS** is in the middle.


---

## Cloud Deployment Models

### Public Cloud

> **📖 Definition:** Cloud resources owned and operated by a third-party cloud service provider (like Microsoft **Azure**), delivered over the internet.

**Characteristics**:
- Resources shared among multiple organizations (multi-tenant)
- Accessible over public internet
- No upfront hardware costs
- Pay only for what you use

**✅ Advantages:**
- **No capital expenditure**: No upfront hardware purchases
- **High scalability**: Unlimited resources on-demand
- **High availability**: Built-in redundancy across regions
- **Low maintenance**: Provider manages hardware and updates

**❌ Disadvantages:**
- **Less control**: Cannot customize underlying infrastructure
- **Specific security requirements**: May not meet certain regulatory needs
- **Shared resources**: Performance can vary

**📋 Common Use Cases:**
- Startups and small businesses
- Web applications with variable traffic
- Development and testing environments
- Big data analytics

****Azure** Example**: Standard **Azure** services available to all customers

### Private Cloud

> **📖 Definition:** Cloud environment dedicated exclusively to one organization, hosted either on-premises or by a third party.

**Characteristics**:
- Single-tenant environment
- Complete control over resources
- Can be hosted on-premises or by a provider
- Greater customization

**✅ Advantages:**
- **Full control**: Complete infrastructure customization
- **Enhanced security**: Dedicated resources, not shared
- **Compliance**: Meet strict regulatory requirements
- **Predictable performance**: Resources not shared

**❌ Disadvantages:**
- **Higher costs**: Must purchase and maintain hardware
- **Limited scalability**: Constrained by physical resources
- **Requires IT expertise**: Need staff to manage infrastructure
- **Maintenance burden**: Responsible for updates and repairs

**📋 Common Use Cases:**
- Government agencies with strict data sovereignty
- Financial institutions with regulatory requirements
- Healthcare organizations (HIPAA compliance)
- Organizations with legacy applications

****Azure** Example**: ****Azure** Stack** - Brings **Azure** services to your **datacenter**

### Hybrid Cloud

> **📖 Definition:** Combination of public and private clouds, connected to allow data and applications to move between them.

**Characteristics**:
- Combines benefits of both public and private
- Flexibility to choose where workloads run
- Data and applications can move between environments
- Unified management tools

**✅ Advantages:**
- **Flexibility**: Choose the best environment for each workload
- **Cost optimization**: Use public cloud for non-sensitive workloads
- **Compliance**: Keep sensitive data in private cloud
- **Business continuity**: Backup and disaster recovery options
- **Gradual migration**: Move to cloud at your own pace

**❌ Disadvantages:**
- **Complexity**: Managing two environments
- **Higher networking costs**: Data transfer between clouds
- **Security challenges**: Multiple points to secure
- **Requires expertise**: Knowledge of both environments

**📋 Common Use Cases:**
- Gradual cloud migration
- Sensitive data must remain on-premises
- Variable workloads (burst to public cloud)
- Disaster recovery and backup

****Azure** Example**: ****Azure** Arc** - Manage on-premises and multi-cloud resources from **Azure**

### Multi-Cloud

> **📖 Definition:** Using services from multiple cloud providers (**Azure**, AWS, Google Cloud) simultaneously.

**Characteristics**:
- Not the same as hybrid cloud
- Prevents vendor lock-in
- Leverages best services from each provider

****Azure** Tool**: ****Azure** Arc** enables multi-cloud management

### Comparison Summary

| Model | Ownership | Location | Best For |
|-------|-----------|----------|----------|
| **Public** | Cloud provider | Provider **datacenter** | General workloads, cost efficiency |
| **Private** | Organization | On-premises or hosted | Regulatory compliance, full control |
| **Hybrid** | Mixed | Both | Gradual migration, mixed requirements |
| **Multi-cloud** | Multiple providers | Multiple providers | Avoiding vendor lock-in |

> **💡 EXAM TIP:** Know when to recommend each model based on scenarios. Look for keywords: "regulatory compliance" = private/hybrid, "lowest cost" = public, "existing on-premises investment" = hybrid.


---

## Consumption-Based Model

### Traditional IT vs Cloud Computing

**Traditional On-Premises (**CapEx**)**:
- Buy servers and equipment upfront (capital expenditure)
- Fixed costs regardless of usage
- Over-provision to handle peak loads
- Responsible for maintenance and upgrades
- Long procurement cycles

**Cloud Computing (**OpEx**)**:
- Pay only for what you use (operational expenditure)
- Variable costs based on consumption
- Scale up or down as needed
- Provider handles maintenance
- Instant provisioning

### How Consumption-Based Pricing Works

**Pay-As-You-Go**:
- Charged based on actual usage
- Billed per second/minute/hour
- No upfront commitment
- Stop paying when you stop using

**✅ Benefits:**
1. **No upfront costs**: Start without large investment
2. **Stop paying when not using**: Turn off resources to save money
3. **Pay for more when needed**: Scale during peak times
4. **Pay for less when not needed**: Scale down during quiet periods
5. **Better cost prediction**: Match expenses to business activity

### Cost Optimization Strategies

1. **Right-sizing**: Use appropriate **VM** sizes for workloads
2. **Auto-shutdown**: Turn off dev/test **VMs** when not in use
3. **Reserved instances**: Commit to 1-3 years for discounts (up to 72%)
4. **Spot instances**: Use spare capacity at steep discounts
5. **Monitoring**: Track and analyze usage patterns

### **CapEx** vs **OpEx**

**Capital Expenditure (**CapEx**)**:
- Upfront investment in physical infrastructure
- Fixed asset that depreciates over time
- Examples: Servers, storage, networking equipment
- Tax deductions spread over multiple years

**Operational Expenditure (**OpEx**)**:
- Ongoing costs for services and products
- Deducted in the same year
- Examples: Cloud subscriptions, software licenses
- More flexible for business

> **💡 EXAM TIP:** Cloud computing shifts spending from **CapEx** to **OpEx**, providing financial flexibility and better cash flow management.


---

## Benefits of Cloud Computing

### High Availability

> **📖 Definition:** Ensuring a service remains accessible and operational with minimal downtime.

**How **Azure** Provides It**:
- **Availability Zones**: Physically separate datacenters within a **region**
- **Region Pairs**: Geographically distant **Azure** regions for disaster recovery
- **Load Balancing**: Distribute traffic across multiple resources
- **Automatic Failover**: Switch to backup systems automatically

**Service Level Agreements (SLAs)**:
- **Azure** guarantees uptime percentages
- 99.9% uptime = ~8.7 hours downtime per year
- 99.95% uptime = ~4.4 hours downtime per year
- 99.99% uptime = ~52 minutes downtime per year

**📋 Use Case:** E-commerce website that must be accessible 24/7

### Scalability

> **📖 Definition:** Ability to increase or decrease resources to match demand.

**Types**:

**Vertical Scaling (Scale Up/Down)**:
- Add more power to existing resources
- Example: Upgrade **VM** from 2 cores to 8 cores
- Limited by hardware constraints
- May require downtime

**Horizontal Scaling (Scale Out/In)**:
- Add more instances of resources
- Example: Add more **VMs** to handle traffic
- Better for cloud environments
- No theoretical limit

****Azure** Tools**:
- **Virtual Machine Scale Sets**: Automatically adjust **VM** count
- **App Service Autoscale**: Scale web apps based on metrics
- ****Azure** Kubernetes Service**: Container orchestration with autoscaling

**📋 Use Case:** Retail website scaling during Black Friday sales

### Elasticity

> **📖 Definition:** Automatic and rapid scaling based on current demand (more dynamic than **scalability**).

**Characteristics**:
- Automatic addition/removal of resources
- Responds to real-time demand
- Can scale both out and in
- Optimizes costs by reducing unused capacity

**Example**: Video streaming service automatically adds servers when users spike during evening hours and removes them at night.

> **💡 EXAM TIP:** Elasticity is automatic and dynamic; **scalability** can be manual or automatic.

### Reliability

> **📖 Definition:** Ability of a system to recover from failures and continue to function.

**How **Azure** Provides It**:
- **Decentralized design**: Services distributed across multiple regions
- **Automatic failover**: Switch to backup resources if primary fails
- **Data replication**: Multiple copies of data across locations
- **Global presence**: 60+ regions worldwide

**✅ Benefits:**
- Applications remain functional during outages
- Data protected against disasters
- Business continuity maintained

**📋 Use Case:** Banking application that must remain operational even during **datacenter** failures

### Predictability

> **📖 Definition:** Confidence in performance and costs.

**Performance Predictability**:
- Autoscaling ensures consistent performance
- Load balancing distributes workload evenly
- High availability maintains service levels
- Geographic distribution reduces latency

**Cost Predictability**:
- **Azure** Pricing Calculator estimates costs
- **Azure** Cost Management tracks spending
- Budget alerts notify when approaching limits
- Pay-as-you-go prevents overspending

**Tools**:
- **Total Cost of Ownership (TCO) Calculator**: Compare on-premises vs **Azure** costs
- **Pricing Calculator**: Estimate **Azure** service costs
- **Cost Management and Billing**: Monitor and optimize spending

> **💡 EXAM TIP:** Predictability has TWO aspects - performance AND cost. Know tools for both.

### Security

> **📖 Definition:** Protection of applications, data, and infrastructure from threats.

****Azure** Security Features**:
- **Microsoft Defender for Cloud**: Unified security management
- ****Azure** DDoS Protection**: Defend against distributed denial-of-service attacks
- ****Azure** Firewall**: Network security and filtering
- **Encryption**: Data encrypted at rest and in transit
- ****Azure** Key Vault**: Secure storage for secrets, keys, certificates
- **Private Link**: Access services over private network

**Compliance**:
- GDPR, HIPAA, ISO 27001, SOC 2
- Industry-specific certifications
- Regular audits and assessments

**Shared Responsibility**: Security is shared between Microsoft and **customer** based on service model

### Governance

> **📖 Definition:** Policies, procedures, and tools to maintain compliance and control.

****Azure** Governance Tools**:
- ****Azure** Policy**: Enforce organizational standards and compliance
- ****Azure** Blueprints**: Define repeatable set of **Azure** resources
- **Resource Locks**: Prevent accidental deletion or modification
- **Role-Based Access Control (**RBAC**)**: Control who can access resources
- **Tags**: Organize and track resources

**✅ Benefits:**
- Ensure compliance with regulations
- Maintain security standards
- Control costs
- Audit resource usage

**📋 Use Case:** Healthcare organization ensuring HIPAA compliance across all resources

### Manageability

> **📖 Definition:** Ease of managing cloud resources.

**Management of the Cloud**:
- **Autoscaling**: Automatically adjust resource levels
- **Template-based deployment**: Use ARM templates for consistent deployments
- **Monitoring and alerts**: Track health and performance
- **Automatic updates**: Provider handles patching and updates

**Management in the Cloud**:
- ****Azure** Portal**: Web-based management console
- ****Azure** CLI**: Command-line interface
- ****Azure** PowerShell**: PowerShell commands for **Azure**
- ****Azure** Mobile App**: Manage on the go
- **REST APIs**: Programmatic access

**✅ Benefits:**
- Single pane of glass for all resources
- Automation reduces manual effort
- Consistent management across environments
- Access from anywhere

> **💡 EXAM TIP:** Manageability has two dimensions - "of" the cloud (how **Azure** manages infrastructure) and "in" the cloud (tools you use to manage your resources).


---

## Chapter Summary

### Key Concepts to Memorize

1. **Cloud Computing**: Delivery of computing services over the internet on a pay-as-you-go basis

2. **Shared Responsibility Model**:
   - Customer always owns: Data, Devices, Accounts
   - Provider always owns: Physical **datacenter**, network, hosts
   - Shared based on service model (**IaaS**, **PaaS**, **SaaS**)

3. **Service Models**:
   - **IaaS**: Maximum control, rent infrastructure (**VMs**, storage, networks)
   - **PaaS**: Focus on apps, provider manages platform (App Service, **SQL Database**)
   - **SaaS**: Fully managed software (Microsoft 365, Teams)

4. **Deployment Models**:
   - **Public**: Shared resources, internet access, low cost
   - **Private**: Dedicated resources, full control, higher cost
   - **Hybrid**: Combination of public and private
   - **Multi-cloud**: Multiple providers

5. **Consumption-Based Model**:
   - Pay only for what you use
   - Convert **CapEx** to **OpEx**
   - Scale up/down as needed

6. **Cloud Benefits**:
   - **High Availability**: Maximum uptime with SLAs
   - **Scalability**: Vertical (up/down) and horizontal (out/in)
   - **Elasticity**: Automatic scaling based on demand
   - **Reliability**: Recover from failures, global distribution
   - **Predictability**: Performance and cost confidence
   - **Security**: Built-in protections and compliance
   - **Governance**: Policies and controls
   - **Manageability**: Easy management tools

### Common Exam Questions

**Question Type 1**: Identify the service model (**IaaS**/**PaaS**/**SaaS**)
- Look for clues about management responsibility
- "Full control over OS" = **IaaS**
- "Focus on application development" = **PaaS**
- "No infrastructure management" = **SaaS**

**Question Type 2**: Match deployment model to scenario
- "Regulatory compliance" → Private or Hybrid
- "Lowest cost" → Public
- "Gradual migration" → Hybrid

**Question Type 3**: Shared responsibility
- Know what **customer** vs provider manages
- Changes based on **IaaS**/**PaaS**/**SaaS**

**Question Type 4**: Benefits and characteristics
- Match benefit to scenario
- Understand **SLA** uptime percentages


---

## Practice Questions

### Question 1
Your company needs to run an application that requires complete control over the operating system. Which cloud service model should you use?

A: **SaaS**

B: **PaaS**

C: **IaaS**

D: Serverless


---

✅ **Answer:** C

💡 **Explanation:** **IaaS** provides full control over the operating system, middleware, and runtime. **PaaS** and **SaaS** abstract these layers.

---


---

### Question 2
Which component is ALWAYS the **customer**'s responsibility in the shared responsibility model?

A: Physical network

B: Operating system

C: Data and information

D: Physical **datacenter**


---

✅ **Answer:** C

💡 **Explanation:** Customers always own their data regardless of service model. Physical infrastructure is always the provider's responsibility.

---


---

### Question 3
A company wants to use Microsoft Teams for communication. What cloud service model is this?

A: **IaaS**

B: **PaaS**

C: **SaaS**

D: Hybrid


---

✅ **Answer:** C

💡 **Explanation:** Microsoft Teams is a fully managed software application delivered as a service.

---


---

### Question 4
What is the primary financial benefit of cloud computing?

A: Increased capital expenditure

B: Fixed monthly costs

C: Converting **CapEx** to **OpEx**

D: Requires large upfront investment


---

✅ **Answer:** C

💡 **Explanation:** Cloud computing eliminates large upfront hardware purchases (**CapEx**) and converts to operational expenses (**OpEx**) based on usage.

---


---

### Question 5
Your company has sensitive data that must remain on-premises due to regulations, but wants to use cloud for other workloads. Which deployment model should you recommend?

A: Public cloud

B: Private cloud

C: Hybrid cloud

D: Multi-cloud


---

✅ **Answer:** C

💡 **Explanation:** Hybrid cloud allows sensitive data to stay on-premises while leveraging public cloud for other workloads.

---


---

### Question 6
What does **elasticity** mean in cloud computing?

A: Resources can be upgraded to higher performance

B: Resources can automatically scale based on demand

C: Resources are distributed globally

D: Resources are encrypted


---

✅ **Answer:** B

💡 **Explanation:** Elasticity is the automatic and dynamic scaling of resources in response to current demand.

---


---

### Question 7
Which **Azure** deployment model allows you to run **Azure** services in your own **datacenter**?

A: Public cloud

B: **Azure** Arc

C: **Azure** Stack

D: Hybrid cloud


---

✅ **Answer:** C

💡 **Explanation:** **Azure** Stack brings **Azure** services to your on-premises **datacenter**, enabling a true private cloud with **Azure** compatibility.

---


---

### Question 8
An **SLA** of 99.9% uptime equals approximately how much downtime per year?

A: 52 minutes

B: 8.7 hours

C: 4.4 hours

D: 1.4 hours


---

✅ **Answer:** B

💡 **Explanation:** 99.9% uptime = 0.1% downtime = 8.76 hours per year. Know common **SLA** percentages for the exam.

---


---

### Question 9
In a **PaaS** model, who is responsible for managing the operating system?

A: Customer

B: Cloud provider

C: Shared between **customer** and provider

D: Third-party vendor


---

✅ **Answer:** B

💡 **Explanation:** In **PaaS**, the provider manages the operating system, middleware, and runtime. Customer focuses on applications and data.

---


---

### Question 10
What is the main difference between **scalability** and **elasticity**?

A: Scalability is automatic, **elasticity** is manual

B: Elasticity is automatic and dynamic, **scalability** can be manual

C: They are the same thing

D: Scalability is for storage, **elasticity** is for compute


---

✅ **Answer:** B

💡 **Explanation:** Elasticity automatically adjusts resources in real-time based on demand. Scalability is the ability to scale but can be manual or scheduled.

---

---


---

## 🎓 Next Steps

Congratulations on completing Chapter 1! You now understand the fundamental concepts of cloud computing.

**Next**: Proceed to [Chapter 2: **Azure** Architecture and Services](02-azure-architecture-services.md) to learn about **Azure**'s global infrastructure and core services.

**Study Tips**:
- Review the practice questions until you can answer them all correctly
- Create flashcards for **IaaS**/**PaaS**/**SaaS** examples
- Draw the shared responsibility model from memory
- Understand WHY each deployment model is used, not just WHAT it is
