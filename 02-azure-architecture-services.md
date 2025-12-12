# 📗 Chapter 2: Azure Architecture and Services

> **📊 Exam Weight:** 35-40% of total exam (LARGEST SECTION)
> **⏱️ Estimated Time:** 4-5 hours
> **📝 Practice Questions:** 10 questions at end of chapter
> **🎯 Learning Objective:** Understand Azure infrastructure and core services

---

## 📖 Chapter Overview

This is the **largest and most important** section of the exam. Understanding Azure's global infrastructure and core services is essential for passing AZ-900.

**What You'll Learn:**
- 🌐 Azure global infrastructure (regions, zones, pairs)
- 💻 Compute services (VMs, containers, serverless)
- 🔗 Networking fundamentals (VNet, VPN, ExpressRoute)
- 💾 Storage services and redundancy options
- 🗄️ Database services (SQL, Cosmos DB, MySQL, PostgreSQL)
- 🔐 Identity, security, and access control
- 🤖 AI and IoT services overview


---

## Table of Contents
1. [**Azure** Global Infrastructure](#azure-global-infrastructure)
2. [**Azure** Compute Services](#azure-compute-services)
3. [**Azure** Networking Services](#azure-networking-services)
4. [**Azure** Storage Services](#azure-storage-services)
5. [**Azure** Database Services](#azure-database-services)
6. [**Azure** Identity and Security Services](#azure-identity-and-security-services)
7. [**Azure** AI and IoT Services](#azure-ai-and-iot-services)
8. [Chapter Summary](#chapter-summary)
9. [Practice Questions](#practice-questions)


---

## **Azure** Global Infrastructure

### **Azure** Regions

> **📖 Definition:** A geographical area containing one or more datacenters networked together with low-latency connections.

**🔑 Key Points:**
- **Azure** has **60+ regions** worldwide (more than any other **cloud provider**)
- Each **region** is at least **300 miles** apart from another **region**
- Regions allow you to deploy resources close to your users for low latency
- Some services are ****region**-specific**, others are **global**

**Examples**:
- East US (Virginia)
- West Europe (Netherlands)
- Southeast Asia (Singapore)
- Australia East (Sydney)

**Choosing a Region**:
1. **Location/Proximity**: Deploy close to users for better performance
2. **Service availability**: Not all services available in all regions
3. **Pricing**: Costs vary by **region**
4. **Compliance**: Data residency requirements

> **💡 EXAM TIP:** Choose regions based on proximity to users, service availability, and compliance requirements.

### Region Pairs

> **📖 Definition:** Each **Azure** **region** is paired with another **region** within the same geography, at least **300 miles** apart.

**Purpose**:
- **Disaster recovery**: If one **region** fails, services can failover to paired **region**
- **Planned maintenance**: Only one **region** in a pair is updated at a time
- **Data residency**: Paired regions within same geography for compliance

**Examples of Region Pairs**:
- East US ↔ West US
- North Europe (Ireland) ↔ West Europe (Netherlands)
- Southeast Asia (Singapore) ↔ East Asia (Hong Kong)

**✅ Benefits:**
- Sequential updates prevent both regions being unavailable
- Data replication across paired regions
- Priority recovery in major outages

> **💡 EXAM TIP:** Region pairs are ALWAYS in the same geography for data residency and compliance.

### Sovereign Regions

> **📖 Definition:** Isolated instances of **Azure** for specific governmental or compliance needs.

**Types**:

****Azure** Government**:
- Dedicated for US government agencies and partners
- Physically isolated from non-government deployments
- Screened US personnel only
- Additional compliance certifications (FedRAMP, DoD)

****Azure** China**:
- Operated by 21Vianet (not Microsoft directly)
- Physically isolated from global **Azure**
- Meets China's regulatory requirements
- Different **Azure** Portal URL

**Other Sovereign Clouds**:
- **Azure** Germany (being migrated to standard regions)

> **💡 EXAM TIP:** Sovereign regions are physically and logically isolated from standard **Azure** for compliance and regulatory requirements.

### Availability Zones

> **📖 Definition:** Physically separate datacenters within an **Azure** **region**, each with independent power, cooling, and networking.

**Characteristics**:
- Minimum of **3 separate zones** in enabled regions
- Each **zone** has one or more datacenters
- Connected with high-speed private fiber networks
- If one **zone** fails, others continue operating

**How to Use**:
- Deploy resources across multiple zones for **high availability**
- **Azure** replicates data across zones automatically
- Zone-redundant services (ZRS) use availability zones

**Supported Services**:
- **Zonal services**: Pin resource to specific **zone** (**VMs**, disks)
- **Zone-redundant services**: Automatically replicate across zones (**SQL Database**, storage)
- **Non-regional services**: Always available, replicated globally (**Azure** AD)

****SLA** Benefits**:
- Single **VM**: 99.9% uptime
- Multiple **VMs** in availability set: 99.95% uptime
- **VMs** across availability zones: **99.99% uptime**

> **💡 EXAM TIP:** Availability zones provide the highest **SLA** (99.99%). Not all regions support availability zones.

### **Azure** Resources and Resource Groups

****Azure** Resource**:
- Any manageable item in **Azure**
- Examples: Virtual machines, storage accounts, databases, virtual networks

**Resource Group**:
- Logical container for grouping related resources
- All resources MUST be in a resource group
- Resources can only be in ONE resource group at a time
- Resource groups cannot be nested

**Best Practices**:
- Group resources by lifecycle (delete together)
- Group by application or project
- Apply permissions at resource group level
- Apply tags for organization and billing

**🔑 Key Points:**
- Deleting a resource group deletes all resources in it
- Resources can interact across resource groups
- Resources can be moved between resource groups
- Resource groups have a location (metadata storage), but resources can be in different regions

> **💡 EXAM TIP:** Deleting a resource group deletes ALL resources within it. This is a common exam question.

### Subscriptions

> **📖 Definition:** Logical unit of **Azure** services linked to an **Azure** account, used for billing and access management.

**Purpose**:
- **Billing boundary**: Separate billing reports and invoices
- **Access control boundary**: Different access management policies
- **Resource limits**: Subscription quotas and limits

**Types**:
- **Free Trial**: $200 credit for 30 days
- **Pay-As-You-Go**: Monthly billing based on usage
- **Enterprise Agreement**: Volume licensing for large organizations
- **Student**: Free services for students

**Multiple Subscription Scenarios**:
- **Environments**: Separate dev, test, and production
- **Organizational structure**: Different departments or teams
- **Billing**: Separate cost tracking per project
- **Limits**: Exceed per-**subscription** resource limits

> **💡 EXAM TIP:** Organizations can have multiple subscriptions for billing separation, access control, and exceeding limits.

### Management Groups

> **📖 Definition:** Container that helps manage access, policies, and compliance across multiple subscriptions.

**Hierarchy**:
```
Root Management Group
  └── Management Group (Production)
      ├── Subscription (Prod-Web)
      └── Subscription (Prod-Database)
  └── Management Group (Development)
      ├── Subscription (Dev-Team1)
      └── Subscription (Dev-Team2)
```

**✅ Benefits:**
- Apply policies across multiple subscriptions
- Organize subscriptions hierarchically
- Inherit access and policies from parent groups
- Up to **6 levels** of depth (not including root)

**📋 Common Use Cases:**
- Enforce **Azure** Policy across all subscriptions
- Provide **RBAC** access to multiple subscriptions
- Organize by business unit, geography, or environment

> **💡 EXAM TIP:** Management groups allow governance at scale across multiple subscriptions.


---

## **Azure** Compute Services

Compute services provide on-demand computing resources for running applications.

### **Azure** Virtual Machines (**VMs**)

> **📖 Definition:** Infrastructure as a Service (**IaaS**) offering providing virtualized Windows or Linux servers.

**📋 Common Use Cases:**
- **Lift and shift**: Migrate on-premises servers to cloud
- **Custom software**: Applications requiring specific OS configurations
- **Development and testing**: Quick provisioning of test environments
- **Extended datacenter**: Add capacity during peak demand

****VM** Components**:
- **Size**: Compute power (CPU, RAM, storage)
- **Image**: Operating system (Windows Server, Ubuntu, RedHat, etc.)
- **Disks**: OS disk, data disks, temporary disk
- **Network**: Virtual network, public/private IP, network security group

****VM** Pricing**:
- Pay per second of usage
- Costs based on size, **region**, OS
- Stop (deallocate) **VM** to stop compute charges (storage still charged)

****VM** Sizes (Categories)**:
- **General Purpose**: Balanced CPU-to-memory (B, D series)
- **Compute Optimized**: High CPU-to-memory (F series)
- **Memory Optimized**: High memory-to-CPU (E, M series)
- **Storage Optimized**: High disk throughput (L series)
- **GPU**: Graphics and deep learning (N series)
- **High Performance Compute**: Fastest CPUs (H series)

> **💡 EXAM TIP:** **VMs** are **IaaS** - you manage OS, applications, data. **Azure** manages physical hardware.

### **Azure** Virtual Machine Scale Sets

> **📖 Definition:** Deploy and manage a set of identical, load-balanced **VMs** that automatically scale.

**Key Features**:
- **Autoscaling**: Automatically increase/decrease **VM** count based on demand or schedule
- **Load balancing**: Built-in load distribution across **VMs**
- **Identical VMs**: All **VMs** created from same image and configuration
- **Up to 1,000 **VM** instances** (or 600 with custom images)

**✅ Benefits:**
- High availability across multiple **VMs**
- Automatic scaling for variable workloads
- Large-scale deployment (hundreds/thousands of **VMs**)
- No extra cost (only pay for **VMs**)

**📋 Common Use Cases:**
- Web applications with variable traffic
- Big data and analytics workloads
- Containerized applications

**Scaling Types**:
- **Manual scaling**: Set specific instance count
- **Scheduled scaling**: Scale at specific times
- **Metric-based scaling**: Scale based on CPU, memory, queue length

> **💡 EXAM TIP:** Scale Sets are for managing multiple identical **VMs** with autoscaling. Use for variable workloads.

### **Azure** Virtual Machine Availability Sets

> **📖 Definition:** Logical grouping of **VMs** to provide redundancy and availability within a **datacenter**.

**Concepts**:

**Fault Domains (FDs)**:
- Physical separation in **datacenter** (different racks)
- Separate power and network switches
- Protects against hardware failures
- Maximum of 3 fault domains

**Update Domains (UDs)**:
- Logical separation for maintenance
- Different **VMs** updated at different times
- Protects against planned maintenance downtime
- Maximum of 20 update domains

**SLA**: 99.95% uptime for **VMs** in availability set

**When to Use**:
- Single **region** **high availability**
- Cannot use with availability zones in same deployment
- No additional cost (only pay for **VMs**)

> **💡 EXAM TIP:** Availability Sets protect against single **datacenter** failures. Availability Zones protect against entire **datacenter** failures (higher **SLA**).

### **Azure** Virtual Desktop

> **📖 Definition:** Desktop and application virtualization service running in the cloud.

**What It Provides**:
- Windows 10/11 desktop experience in the cloud
- Access from any device (Windows, Mac, iOS, Android, web browser)
- Centralized management and security
- Multi-session Windows 10/11 (unique to **Azure**)

**✅ Benefits:**
- **Security**: Data stays in **Azure**, not on user devices
- **Centralized management**: IT controls apps and updates
- **Cost savings**: Multi-session reduces **VM** costs
- **Compliance**: Data remains in compliant regions
- **Productivity**: Access from anywhere

**📋 Common Use Cases:**
- Remote work and work-from-home
- Contractors and temporary workers
- Software development and testing
- Legacy application access

> **💡 EXAM TIP:** **Azure** Virtual Desktop is for providing virtual desktops to users, not for running server workloads.

### **Azure** Containers

> **📖 Definition:** Lightweight, portable, self-contained environments for running applications.

**Benefits Over VMs**:
- **Faster startup**: Seconds vs minutes
- **Smaller size**: MBs vs GBs
- **Higher density**: More containers per host
- **Portability**: Run anywhere (dev, test, prod, multi-cloud)

****Azure** Container Services**:

****Azure** Container Instances (ACI)**:
- Simplest way to run containers
- No orchestration needed
- Fast startup (seconds)
- Per-second billing
- Good for: Isolated containers, batch jobs, event-driven applications

****Azure** Kubernetes Service (AKS)**:
- Managed Kubernetes (container orchestration)
- Automates deployment, scaling, management
- Built-in monitoring and logging
- Good for: Microservices, complex applications, container orchestration

****Azure** Container Apps**:
- Fully managed serverless container service
- Built on Kubernetes but abstracted
- Auto-scaling, load balancing, rolling updates
- Good for: Microservices, APIs, event-driven apps

> **💡 EXAM TIP:** ACI for simple containers, AKS for orchestrated multi-container applications requiring Kubernetes.

### **Azure** Functions

> **📖 Definition:** Serverless compute service that runs code in response to events without managing infrastructure.

**Characteristics**:
- **Event-driven**: Triggered by events (HTTP, timer, queue message, database change)
- **Serverless**: No infrastructure management
- **Auto-scaling**: Scales automatically based on demand
- **Pay per execution**: Charged only when code runs (not idle time)
- **Stateless**: Each execution is independent (can use Durable Functions for stateful)

**Common Triggers**:
- HTTP request (REST API)
- Timer (scheduled tasks)
- **Azure** Queue message
- **Azure** Blob upload
- Database changes

**📋 Common Use Cases:**
- REST APIs and webhooks
- Scheduled tasks (cleanup, reports)
- Data processing pipelines
- Event-driven automation
- IoT data processing

**Pricing**:
- **Consumption plan**: Pay per execution and execution time
- **Premium plan**: Always-ready instances, unlimited duration
- **App Service plan**: Run on dedicated **VMs**

> **💡 EXAM TIP:** **Azure** Functions = serverless, event-driven, pay per execution. Use when you need code triggered by events without managing servers.

### **Azure** App Service

> **📖 Definition:** Fully managed **PaaS** for building, deploying, and scaling web apps.

**Supported App Types**:
- **Web Apps**: Host websites and web applications (ASP.NET, Java, Node.js, Python, PHP)
- **API Apps**: REST APIs with Swagger support
- **Mobile Apps**: Mobile backends
- **Web Jobs**: Background tasks

**Key Features**:
- **Built-in autoscaling**: Scale based on demand
- **Deployment slots**: Blue/green deployments, testing in production
- **Continuous deployment**: Integrate with GitHub, **Azure** DevOps, Bitbucket
- **Custom domains and SSL**: Bring your own domain and certificates
- **Authentication**: Built-in auth with **Azure** AD, Google, Facebook, Twitter

**App Service Plans**:
- Defines compute resources for web apps
- Multiple apps can run on same plan
- Pricing tiers: Free, Shared, Basic, Standard, Premium, Isolated

**✅ Benefits:**
- No infrastructure management (**PaaS**)
- Focus on code, not servers
- Built-in load balancing and **high availability**
- Integrated monitoring and diagnostics

**📋 Common Use Cases:**
- Web applications and websites
- REST APIs
- Mobile backends
- Continuous deployment workflows

> **💡 EXAM TIP:** App Service is **PaaS** - you deploy code, **Azure** manages infrastructure. Supports multiple languages and frameworks.

### Comparison: When to Use Each Compute Service

| Service | Type | Use When | Management Level |
|---------|------|----------|------------------|
| **Virtual Machines** | **IaaS** | Full control needed, custom OS, lift-and-shift | High (you manage OS) |
| ****VM** Scale Sets** | **IaaS** | Autoscaling identical **VMs**, variable workloads | High |
| **Virtual Desktop** | DaaS | Remote desktop access, virtual workspaces | Medium |
| **Container Instances** | CaaS | Simple containers, no orchestration | Low |
| **Kubernetes Service** | CaaS | Container orchestration, microservices | Medium |
| **Functions** | Serverless | Event-driven, short tasks, pay per execution | Very Low |
| **App Service** | **PaaS** | Web apps, APIs, focus on code not infrastructure | Low |

> **💡 EXAM TIP:** Match the service to the scenario based on control needs and workload type.


---

## **Azure** Networking Services

### **Azure** Virtual Network (**VNet**)

> **📖 Definition:** Isolated network in **Azure** for your resources to communicate securely.

**Key Concepts**:
- **Address space**: IP range for the **VNet** (CIDR notation, e.g., 10.0.0.0/16)
- **Subnets**: Divide **VNet** into smaller networks
- **Private IPs**: Resources communicate privately within **VNet**
- **Isolation**: Each **VNet** is isolated from others by default

**Features**:
- **Communication**: Resources in same **VNet** can communicate
- **Segmentation**: Use subnets to organize and secure resources
- **Routing**: **Azure** handles routing between subnets automatically
- **Filtering**: Network Security Groups (NSGs) control traffic

**📋 Common Use Cases:**
- Isolate and segment workloads
- Connect on-premises networks (hybrid)
- Secure communication between **Azure** resources

> **💡 EXAM TIP:** VNets provide network isolation and private communication for **Azure** resources.

### Network Security Groups (NSG)

> **📖 Definition:** Firewall rules that control inbound and outbound traffic to **Azure** resources.

**How It Works**:
- Contains security rules (allow/deny)
- Rules evaluated by priority (lower number = higher priority)
- Applied to subnets or network interfaces
- Stateful firewall (return traffic automatically allowed)

**Rule Properties**:
- **Priority**: 100-4096 (lower = higher priority)
- **Source/Destination**: IP address, range, service tag
- **Port**: Specific port or range
- **Protocol**: TCP, UDP, ICMP, Any
- **Action**: Allow or Deny

**Default Rules** (cannot be deleted):
- Allow **VNet** traffic
- Allow **Azure** Load Balancer
- Deny all other inbound
- Allow all outbound to internet

> **💡 EXAM TIP:** NSGs are like firewalls controlling traffic to/from resources based on rules with priorities.

### **Azure** **VPN Gateway**

> **📖 Definition:** Sends encrypted traffic between **Azure** and on-premises networks over the public internet.

**Types**:

**Site-to-Site (S2S)**:
- Connects entire on-premises network to **Azure** **VNet**
- Requires VPN device on-premises
- Multiple users/devices access **Azure**
- Good for: Hybrid infrastructure

**Point-to-Site (P2S)**:
- Individual device connects to **Azure** **VNet**
- No VPN device required
- Good for: Remote workers, individual access

****VNet**-to-VNet**:
- Connects two **Azure** VNets
- Can be in different regions
- Encrypted traffic over Microsoft backbone

**Characteristics**:
- Encrypted connection over internet
- Maximum bandwidth: Up to 10 Gbps (depending on SKU)
- Cost-effective for hybrid connectivity
- Higher latency than **ExpressRoute**

> **💡 EXAM TIP:** **VPN Gateway** uses internet (encrypted). Site-to-Site for office, Point-to-Site for individuals.

### **Azure** **ExpressRoute**

> **📖 Definition:** Private, dedicated connection between on-premises and **Azure** that doesn't go over the internet.

**✅ Benefits:**
- **Higher speeds**: Up to 100 Gbps
- **Lower latency**: Doesn't traverse internet
- **More reliable**: Dedicated connection
- **More secure**: Traffic doesn't go over public internet
- **Consistent performance**: Predictable throughput

**Connection Models**:
- **CloudExchange co-location**: Datacenter at same facility as exchange provider
- **Point-to-point Ethernet**: Dedicated connection to **Azure**
- **Any-to-any (IPVPN)**: Integrate **Azure** into WAN
- ****ExpressRoute** Direct**: Connect directly to Microsoft's global network

**📋 Common Use Cases:**
- Large-scale data migration
- Hybrid applications requiring low latency
- Disaster recovery and backup
- Regulatory/compliance requirements (data can't traverse internet)

**Comparison: **VPN Gateway** vs ExpressRoute**

| Feature | **VPN Gateway** | **ExpressRoute** |
|---------|-------------|--------------|
| **Connection** | Over internet (encrypted) | Private dedicated line |
| **Speed** | Up to 10 Gbps | Up to 100 Gbps |
| **Latency** | Higher (internet) | Lower (dedicated) |
| **Cost** | Lower | Higher |
| **Use Case** | Small/medium workloads | Mission-critical, large-scale |

> **💡 EXAM TIP:** **ExpressRoute** = private connection, NOT over internet, higher cost, better performance. **VPN Gateway** = over internet (encrypted), lower cost.

### **Azure** DNS

> **📖 Definition:** Hosting service for DNS domains using **Azure** infrastructure.

**Features**:
- Host your DNS domains in **Azure**
- Manage DNS records (A, AAAA, CNAME, MX, TXT, etc.)
- Use **Azure**'s global anycast network
- Integrated with **Azure** services
- Role-based access control

**✅ Benefits:**
- High availability and performance (100% uptime **SLA**)
- Global distribution with low latency
- Integrated with other **Azure** services
- Manage from **Azure** Portal, CLI, PowerShell

**What It Does NOT Do**:
- Cannot buy domain names (use third-party registrar)
- Purchase domains elsewhere, host DNS in **Azure**

> **💡 EXAM TIP:** **Azure** DNS hosts your DNS zones and records but doesn't sell domain names.

### Load Balancing Services

****Azure** Load Balancer**:
- **Layer**: 4 (Transport - TCP/UDP)
- **Scope**: Regional
- **Type**: Internal or Public
- **Use case**: Distribute traffic across **VMs** in same **region**

****Azure** Application Gateway**:
- **Layer**: 7 (Application - HTTP/HTTPS)
- **Features**: URL-based routing, SSL termination, Web Application Firewall (WAF)
- **Scope**: Regional
- **Use case**: Load balance web applications with advanced routing

****Azure** Front Door**:
- **Layer**: 7 (Application)
- **Scope**: Global
- **Features**: Global load balancing, CDN, WAF, SSL offload
- **Use case**: Global web applications, low latency worldwide

****Azure** Traffic Manager**:
- **Layer**: DNS-level
- **Scope**: Global
- **Method**: DNS-based traffic routing
- **Use case**: Distribute traffic across global regions based on routing rules

**Comparison**:

| Service | Layer | Scope | Best For |
|---------|-------|-------|----------|
| **Load Balancer** | 4 (TCP/UDP) | Regional | **VM** load balancing |
| **Application Gateway** | 7 (HTTP/HTTPS) | Regional | Web apps with advanced routing |
| **Front Door** | 7 (HTTP/HTTPS) | Global | Global web apps, CDN |
| **Traffic Manager** | DNS | Global | Global DNS-based routing |

> **💡 EXAM TIP:** Know the layer (4 vs 7), scope (regional vs global), and use case for each load balancing service.


---

## **Azure** Storage Services

### Storage Account

> **📖 Definition:** Provides a unique namespace for your **Azure** Storage data, accessible worldwide via HTTP/HTTPS.

**Storage Account Types**:
- **Standard (General-purpose v2)**: Most common, supports all services (Blob, File, Queue, Table)
- **Premium block blobs**: High performance for blobs
- **Premium file shares**: High performance for file shares
- **Premium page blobs**: For **VMs** and disks

**Performance Tiers**:
- **Standard**: HDD-backed, lower cost
- **Premium**: SSD-backed, higher performance, higher cost

**Access Tiers** (for Blob storage):
- **Hot**: Frequently accessed data, higher storage cost, lower access cost
- **Cool**: Infrequently accessed (stored 30+ days), lower storage cost, higher access cost
- **Cold**: Rarely accessed (stored 90+ days), even lower storage cost
- **Archive**: Rarely accessed (stored 180+ days), lowest storage cost, highest access cost, retrieval latency hours

> **💡 EXAM TIP:** Choose access tier based on how frequently data is accessed. Hot = frequent, Archive = rare.

### **Azure** Storage Redundancy

Critical for exam - understand all redundancy options.

**Locally Redundant Storage (LRS)**:
- **Copies**: 3 copies in single **datacenter**
- **Durability**: 99.999999999% (11 nines)
- **Protection**: Hardware failures within **datacenter**
- **Cost**: Lowest
- **Use case**: Non-critical data, data can be recreated

**Zone-Redundant Storage (ZRS)**:
- **Copies**: 3 copies across 3 availability zones in same **region**
- **Durability**: 99.9999999999% (12 nines)
- **Protection**: Datacenter-level failures
- **Cost**: Medium
- **Use case**: High availability within **region**

**Geo-Redundant Storage (GRS)**:
- **Copies**: 6 copies (3 local + 3 in paired **region**)
- **Durability**: 99.99999999999999% (16 nines)
- **Protection**: Regional outages
- **Read access**: No (unless RA-GRS)
- **Cost**: Higher
- **Use case**: Disaster recovery, regional outages

**Geo-Zone-Redundant Storage (GZRS)**:
- **Copies**: 6 copies (3 across zones + 3 in paired **region**)
- **Durability**: 99.99999999999999% (16 nines)
- **Protection**: Zone AND regional failures
- **Cost**: Highest
- **Use case**: Maximum durability and availability

**Read-Access GRS (RA-GRS)** and **RA-GZRS**:
- Same as GRS/GZRS but with read access to secondary **region**
- Good for: Applications that can read from secondary during primary outage

**Redundancy Comparison Table**:

| Redundancy | Copies | Locations | Durability (9s) | Protects Against |
|------------|--------|-----------|-----------------|------------------|
| **LRS** | 3 | 1 **datacenter** | 11 | Hardware failure |
| **ZRS** | 3 | 3 zones | 12 | Datacenter failure |
| **GRS** | 6 | 2 regions | 16 | Regional failure |
| **GZRS** | 6 | 3 zones + **region** | 16 | Zone + regional failure |

> **💡 EXAM TIP:** Know the number of copies, where they're stored, and what each protects against. Common exam question!

### **Azure** **Blob Storage**

> **📖 Definition:** Object storage for massive amounts of unstructured data (text, binary, images, videos, logs).

**Blob Types**:
- **Block blobs**: Text and binary files, up to 190.7 TB
- **Append blobs**: Optimized for append operations (logs)
- **Page blobs**: Random access files, VHD files for **VMs**, up to 8 TB

**📋 Common Use Cases:**
- Serving images/documents to browser
- Storing files for distributed access
- Streaming video and audio
- Backup and disaster recovery
- Data lakes for analytics
- Log files

**Access Methods**:
- **Azure** Portal
- REST API
- **Azure** Storage Explorer
- **Azure** CLI / PowerShell
- SDKs (Python, .NET, Java, etc.)

> **💡 EXAM TIP:** Blob = object storage for unstructured data. Think files, images, videos, backups.

### **Azure** Files

> **📖 Definition:** Fully managed file shares in the cloud accessible via SMB and NFS protocols.

**Key Features**:
- Standard file share protocol (SMB 2.1, 3.0, 3.1.1)
- Mount from Windows, Linux, macOS
- Replace or supplement on-premises file servers
- Accessible from anywhere with internet connection

**📋 Common Use Cases:**
- **Lift and shift**: Replace on-premises file servers
- **Shared application data**: Multiple **VMs** access same files
- **Developer tools**: Share tools and configs across team
- **Hybrid scenarios**: Sync with on-premises using **Azure** File Sync

**✅ Benefits:**
- No server management required
- Highly available with redundancy options
- Accessible via standard file protocols
- Snapshot capability for backups

> **💡 EXAM TIP:** **Azure** Files = cloud file share accessible via SMB. Think shared folders, replacing file servers.

### **Azure** Queue Storage

> **📖 Definition:** Message queue for storing large numbers of messages, accessed from anywhere.

**Characteristics**:
- Store millions of messages
- Each message up to 64 KB
- Asynchronous communication between components
- FIFO (First In, First Out) processing

**📋 Common Use Cases:**
- Decouple application components
- Asynchronous task processing
- Work queue for background jobs
- Communication between web and worker roles

> **💡 EXAM TIP:** Queue Storage = message queuing for asynchronous communication between app components.

### **Azure** Table Storage

> **📖 Definition:** NoSQL key-value store for structured, non-relational data.

**Characteristics**:
- Schema-less design
- Fast queries using keys
- Cost-effective for large datasets
- Suitable for semi-structured data

**📋 Common Use Cases:**
- User data for web applications
- Device information for IoT
- Metadata and configuration
- Any dataset that doesn't require complex joins

> **ℹ️ Note:** For more advanced NoSQL, consider ****Azure** Cosmos DB**.

> **💡 EXAM TIP:** Table Storage = NoSQL key-value store for semi-structured data.

### **Azure** Disk Storage

> **📖 Definition:** Block-level storage volumes for **Azure** Virtual Machines.

**Disk Types**:
- **Ultra Disk**: Highest performance, I/O intensive workloads (SAP HANA, SQL Server)
- **Premium SSD**: Production workloads, high performance
- **Standard SSD**: Web servers, dev/test, low IOPS workloads
- **Standard HDD**: Backups, non-critical, lowest cost

**Disk Roles**:
- **OS Disk**: Contains operating system
- **Data Disk**: Store application data
- **Temporary Disk**: Short-term storage (lost on **VM** deallocate)

**Managed vs Unmanaged Disks**:
- **Managed** (recommended): **Azure** manages storage account, handles scaling, replication
- **Unmanaged**: You manage storage accounts manually

> **💡 EXAM TIP:** Choose disk type based on performance needs and cost. Managed disks are recommended.

### **Azure** Data Migration Tools

**AzCopy**:
- **Type**: Command-line utility
- **Purpose**: Copy blobs or files to/from storage accounts
- **Use case**: One-time migrations, scripting
- **Features**: Fast, efficient, can sync directories

****Azure** Storage Explorer**:
- **Type**: GUI application
- **Purpose**: Manage **Azure** Storage (upload, download, manage blobs/files/queues/tables)
- **Platform**: Windows, Mac, Linux
- **Use case**: Interactive storage management

****Azure** File Sync**:
- **Type**: Service
- **Purpose**: Sync on-premises file servers with **Azure** Files
- **✅ Benefits:** Cloud tiering (free up local space), multi-site access
- **Use case**: Hybrid file server scenarios

****Azure** Data Box**:
- **Type**: Physical device
- **Purpose**: Transfer massive amounts of data (TBs/PBs) to **Azure**
- **Process**: Microsoft ships device → You copy data → Ship back → Microsoft uploads
- **Sizes**: Data Box (80 TB), Data Box Disk (40 TB), Data Box Heavy (1 PB)
- **Use case**: Limited bandwidth, large initial migrations, regular bulk uploads

**Comparison**:

| Tool | Type | Best For | Data Size |
|------|------|----------|-----------|
| **AzCopy** | CLI | Scripted transfers | GBs to TBs |
| **Storage Explorer** | GUI | Interactive management | Small to medium |
| **File Sync** | Service | Hybrid file server sync | Ongoing sync |
| **Data Box** | Physical device | Massive offline transfer | TBs to PBs |

> **💡 EXAM TIP:** Data Box for massive data transfer when network is too slow. AzCopy for scripting. File Sync for hybrid scenarios.


---

## **Azure** Database Services

### **Azure** **SQL Database**

> **📖 Definition:** Fully managed relational database (**PaaS**) based on Microsoft SQL Server.

**Key Features**:
- **Fully managed**: Automatic backups, patching, **high availability**
- **Scalability**: Scale up/down based on demand
- **Built-in intelligence**: Automatic tuning, threat detection
- **High availability**: 99.99% **SLA**
- **Compatibility**: Works with SQL Server tools and applications

**Deployment Options**:
- **Single Database**: One database with dedicated resources
- **Elastic Pool**: Multiple databases share resources (cost-effective)
- **Managed Instance**: Near 100% compatibility with on-premises SQL Server

**📋 Common Use Cases:**
- Modern cloud applications
- Migrating SQL Server applications to cloud
- Need for automatic backups and patching
- Applications requiring relational database

> **💡 EXAM TIP:** **Azure** **SQL Database** is **PaaS** - Microsoft manages infrastructure, backups, patching, **high availability**.

### **Azure** **Cosmos DB**

> **📖 Definition:** Globally distributed, multi-model NoSQL database service.

**Key Features**:
- **Global distribution**: Replicate data to any **Azure** **region** with one click
- **Low latency**: Single-digit millisecond response times
- **Multiple APIs**: SQL, MongoDB, Cassandra, Gremlin, Table
- **Elastic scale**: Throughput and storage scale independently
- **99.999% availability SLA** (with multi-**region**)

**📋 Common Use Cases:**
- IoT and telemetry data
- Gaming leaderboards
- Mobile applications
- Real-time analytics
- E-commerce catalogs and shopping carts
- Global applications requiring low latency

**✅ Benefits:**
- No schema management
- Automatic indexing
- Turnkey global distribution
- Guaranteed performance with SLAs

> **💡 EXAM TIP:** **Cosmos DB** = globally distributed NoSQL, multiple APIs, low latency, mission-critical applications.

### **Azure** Database for MySQL/PostgreSQL

> **📖 Definition:** Fully managed versions of popular open-source databases.

****Azure** Database for MySQL**:
- Based on MySQL Community Edition
- Compatible with existing MySQL applications
- Built-in **high availability**
- Automatic backups

****Azure** Database for PostgreSQL**:
- Based on PostgreSQL
- Supports extensions
- Two deployment options: Single Server, Flexible Server
- Advanced data types and indexing

**✅ Benefits:**
- No database administration required
- Automatic patching and backups
- Built-in monitoring and security
- 99.99% **SLA**

**📋 Common Use Cases:**
- Migrating MySQL/PostgreSQL applications to cloud
- Open-source database preference
- Applications built with popular frameworks (Django, Ruby on Rails)

> **💡 EXAM TIP:** **Azure** manages these open-source databases as **PaaS** - you focus on apps, **Azure** manages infrastructure.

### Database Comparison

| Database | Type | Best For |
|----------|------|----------|
| **SQL Database** | Relational (SQL Server) | Relational data, migrations from SQL Server |
| **Cosmos DB** | NoSQL (multi-model) | Global apps, low latency, NoSQL workloads |
| **MySQL** | Relational (open-source) | MySQL applications, LAMP stack |
| **PostgreSQL** | Relational (open-source) | PostgreSQL applications, advanced features |

> **💡 EXAM TIP:** Choose based on workload - relational = SQL/MySQL/PostgreSQL, NoSQL/global = **Cosmos DB**.


---

## **Azure** Identity and Security Services

### **Azure** Active Directory (**Azure** AD)

> **📖 Definition:** Microsoft's cloud-based identity and access management service.

**What It Does**:
- **Authentication**: Verify identity of users
- **Single Sign-On (**SSO**)**: One identity for multiple applications
- **Application management**: Manage access to cloud and on-premises apps
- **Device management**: Register and manage devices

****Azure** AD vs Active Directory Domain Services (AD DS)**:
- **AD DS**: On-premises, uses Kerberos/NTLM, domain controllers
- ****Azure** AD**: Cloud-based, uses HTTP/HTTPS (REST APIs), modern protocols (SAML, OAuth, OpenID)

**Key Concepts**:
- **Tenant**: Dedicated instance of **Azure** AD for an organization
- **Identity**: User, application, or service that can be authenticated
- **Account**: Identity with associated data

**Who Uses **Azure** AD**:
- **IT Administrators**: Manage user access and security
- **App Developers**: Add authentication to applications
- **Users**: Sign in to Microsoft 365, **Azure** Portal, **SaaS** apps
- **Online service subscribers**: Microsoft 365, **Azure**, Dynamics 365

> **💡 EXAM TIP:** **Azure** AD is for identity and access management in the cloud. Different from on-premises AD DS.

### Authentication Methods

**Single Sign-On (**SSO**)**:
- Sign in once, access multiple applications
- Reduces password fatigue
- Improves security (fewer passwords to manage)
- Better user experience

**Multi-Factor Authentication (**MFA**)**:
- Requires two or more verification methods:
  - **Something you know**: Password
  - **Something you have**: Phone, hardware token
  - **Something you are**: Fingerprint, face recognition
- Significantly increases security
- Free for administrators, paid for users (**Azure** AD Premium)

**Passwordless Authentication**:
- **Windows Hello for Business**: Biometric or PIN
- **Microsoft Authenticator App**: Approve sign-in on phone
- **FIDO2 Security Keys**: Physical security keys
- **✅ Benefits:** More secure than passwords, better user experience

> **💡 EXAM TIP:** **MFA** requires 2+ factors. Passwordless eliminates passwords entirely for better security and UX.

### External Identities

****Azure** AD B2B (Business-to-Business)**:
- Collaborate with external partners
- Partners use their own credentials
- No need to manage external identities
- Use case: Partner collaboration, vendor access

****Azure** AD B2C (Business-to-Consumer)**:
- Customer identity management for consumer apps
- Supports social accounts (Google, Facebook, local accounts)
- Customizable sign-up/sign-in experiences
- Use case: Customer-facing applications

> **💡 EXAM TIP:** B2B = partners use their own identities. B2C = **customer** identity for apps.

### Conditional Access

> **📖 Definition:** Policies that enforce access requirements based on conditions.

**How It Works**:
- **Signals**: User, location, device, application, risk level
- **Decisions**: Allow, block, require **MFA**
- **Enforcement**: Applied before granting access

**Example Policies**:
- Require **MFA** for administrators
- Block access from untrusted locations
- Require compliant device for accessing company data
- Require password change if risk detected

**✅ Benefits:**
- Adaptive security based on context
- Protect against compromised credentials
- Enforce compliance requirements

**Requirement**: **Azure** AD Premium P1

> **💡 EXAM TIP:** Conditional Access = if/then policies for access control based on signals like location, device, risk.

### Role-Based Access Control (**RBAC**)

> **📖 Definition:** Authorization system for managing access to **Azure** resources based on roles.

**How It Works**:
- Assign roles to users, groups, or service principals
- Roles define what actions are allowed
- Applied at scope: Management group, **subscription**, resource group, or resource
- Inheritance: Child scopes inherit permissions from parent

**Built-in Roles**:
- **Owner**: Full access including ability to delegate
- **Contributor**: Create and manage resources, cannot grant access
- **Reader**: View resources only, no modifications
- **User Access Administrator**: Manage user access to resources

**Custom Roles**: Create specific roles for your organization's needs

**Scopes** (from broad to narrow):
1. Management Group
2. Subscription
3. Resource Group
4. Resource

> **💡 EXAM TIP:** **RBAC** controls WHO can do WHAT to WHICH resources. Know Owner, Contributor, Reader roles.

### Zero Trust Security Model

**Principle**: "Never trust, always verify" - assume breach and verify every request.

**Core Principles**:
1. **Verify explicitly**: Always authenticate and authorize
2. **Use least privilege**: Minimum access needed
3. **Assume breach**: Minimize blast radius and segment access

**Implementation**:
- Require **MFA** for all users
- Conditional Access policies
- Segment networks
- Encrypt data
- Monitor and detect threats

> **💡 EXAM TIP:** Zero Trust = verify every access request, never assume trust based on network location.

### Defense in Depth

> **📖 Definition:** Layered security approach with multiple levels of protection.

**Layers** (from outer to inner):
1. **Physical security**: Datacenter access control
2. **Identity and access**: **MFA**, **RBAC**, Conditional Access
3. **Perimeter**: DDoS protection, firewalls
4. **Network**: Segmentation, NSGs, deny by default
5. **Compute**: Secure **VMs**, patch management
6. **Application**: Secure development, no secrets in code
7. **Data**: Encryption at rest and in transit

**Principle**: If one layer fails, others still provide protection.

> **💡 EXAM TIP:** Defense in Depth = multiple layers of security. Know the layers from physical to data.

### Microsoft Defender for Cloud

> **📖 Definition:** Unified security management and threat protection across **Azure**, on-premises, and multi-cloud.

**Key Features**:
- **Security posture management**: Recommendations to improve security
- **Threat protection**: Detect and respond to threats
- **Compliance**: Track compliance with regulatory standards
- **Secure score**: Metric showing current security posture
- **Workload protection**: Protect **VMs**, databases, containers, etc.

**Capabilities**:
- Continuous security assessment
- Just-in-time **VM** access
- Adaptive application controls
- File integrity monitoring
- Network map and hardening

**Pricing**:
- **Free tier**: Basic security recommendations
- **Paid tier**: Advanced threat protection, regulatory compliance

> **💡 EXAM TIP:** Defender for Cloud provides security recommendations, threat protection, and compliance tracking.


---

## **Azure** AI and IoT Services

### **Azure** AI Services

****Azure** Cognitive Services**:
- Pre-built AI models accessible via APIs
- No AI expertise required
- Categories:
  - **Vision**: Computer Vision, Face API, Form Recognizer
  - **Speech**: Speech-to-text, text-to-speech, translation
  - **Language**: Text analytics, translation, Q&A
  - **Decision**: Content moderation, anomaly detection

****Azure** Machine Learning**:
- Platform for building, training, deploying ML models
- Automated ML capabilities
- MLOps for model lifecycle management
- Use case: Data scientists building custom models

****Azure** Bot Service**:
- Build conversational AI bots
- Integrate with multiple channels (Teams, Slack, web)
- Use case: Customer service chatbots

> **💡 EXAM TIP:** Cognitive Services = pre-built AI APIs. Machine Learning = build custom models.

### **Azure** IoT Services

****Azure** IoT Hub**:
- Central message hub for bi-directional communication with IoT devices
- Supports millions of devices
- Device management and security
- Use case: Collect telemetry from IoT devices

****Azure** IoT Central**:
- Fully managed **SaaS** solution for IoT
- No cloud expertise required
- Pre-built templates for common scenarios
- Use case: Quick IoT deployment without building infrastructure

****Azure** Sphere**:
- Secure end-to-end IoT solution
- Includes certified hardware, OS, and cloud service
- Use case: Highly secured IoT devices

**Comparison**:

| Service | Type | Complexity | Best For |
|---------|------|------------|----------|
| **IoT Hub** | **PaaS** | Medium | Custom IoT solutions |
| **IoT Central** | **SaaS** | Low | Quick deployment, pre-built templates |
| ****Azure** Sphere** | End-to-end | Low | Maximum security for devices |

> **💡 EXAM TIP:** IoT Hub = custom solutions with control. IoT Central = quick **SaaS** solution. Sphere = maximum security.


---

## Chapter Summary

### 🎯 Key Takeaways

> **💡 QUICK RECAP:**
> 

**Global Infrastructure**:
- **Regions**: 60+ worldwide, deploy close to users
- **Region Pairs**: Disaster recovery, 300+ miles apart
- **Availability Zones**: 3+ separate datacenters per **region**, 99.99% **SLA**
- **Resource Groups**: Logical containers for resources
- **Subscriptions**: Billing and access boundary
- **Management Groups**: Organize multiple subscriptions

**Compute Services**:
- **VMs**: **IaaS**, full control, lift-and-shift
- ****VM** Scale Sets**: Autoscaling identical **VMs**
- **Virtual Desktop**: Cloud-based desktops
- **Containers**: ACI (simple), AKS (orchestrated)
- **Functions**: Serverless, event-driven, pay per execution
- **App Service**: **PaaS** for web apps and APIs

**Networking**:
- **VNet**: Isolated networks, private communication
- **NSG**: Firewall rules for traffic control
- **VPN Gateway**: Encrypted connection over internet
- **ExpressRoute**: Private dedicated connection
- **Load Balancers**: Layer 4 (regional), Layer 7 (Application Gateway, Front Door)

**Storage**:
- **Redundancy**: LRS (1 **datacenter**), ZRS (3 zones), GRS (2 regions), GZRS (zones + regions)
- **Blob**: Object storage (files, images, videos)
- **Files**: Cloud file shares (SMB)
- **Queue**: Message queuing
- **Table**: NoSQL key-value
- **Disks**: **VM** storage (Ultra, Premium, Standard)
- **Migration**: AzCopy (CLI), Data Box (physical)

**Databases**:
- **SQL Database**: Managed SQL Server (**PaaS**)
- **Cosmos DB**: Global NoSQL, low latency
- **MySQL/PostgreSQL**: Managed open-source databases

**Identity & Security**:
- ****Azure** AD**: Cloud identity service
- **Authentication**: **SSO**, **MFA**, Passwordless
- **RBAC**: Role-based access control
- **Zero Trust**: Never trust, always verify
- **Defense in Depth**: Layered security
- **Defender for Cloud**: Security management and threat protection


---

## Practice Questions

### Question 1
Your company needs to ensure **VMs** remain available even if an entire **Azure** **datacenter** fails. What should you use?

A: Availability Set

B: Availability Zones

C: **VM** Scale Set

D: Load Balancer


<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** Availability Zones protect against **datacenter**-level failures with physically separate datacenters. Availability Sets protect against failures within a single **datacenter**.

</details>



---

### Question 2
Which storage redundancy option provides protection against regional disasters at the lowest cost?

A: LRS

B: ZRS

C: GRS

D: GZRS


<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** GRS replicates data to a secondary **region** (6 copies total) protecting against regional disasters. GZRS also does this but costs more due to **zone** redundancy.

</details>



---

### Question 3
Your application needs to run code in response to messages in a queue without managing servers. Which service should you use?

A: **Azure** App Service

B: **Azure** Functions

C: **Azure** Virtual Machines

D: **Azure** Kubernetes Service


<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** **Azure** Functions is serverless and event-driven, perfect for responding to queue messages without managing infrastructure.

</details>



---

### Question 4
Which connection type provides a private, dedicated connection to **Azure** that doesn't go over the internet?

A: **VPN Gateway** Site-to-Site

B: **VPN Gateway** Point-to-Site

C: **Azure** **ExpressRoute**

D: Virtual Network Peering


<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** **ExpressRoute** provides a private, dedicated connection that doesn't traverse the public internet. **VPN Gateway** connections go over the internet (though encrypted).

</details>



---

### Question 5
You need to enforce **MFA** for all users accessing the **Azure** Portal from outside the corporate network. What should you use?

A: **Azure** Policy

B: Conditional Access

C: **RBAC**

D: Network Security Group


<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** Conditional Access creates if/then policies based on signals like location. It can require **MFA** for access from outside the network.

</details>



---

### Question 6
Which **Azure** service is best for hosting a globally distributed e-commerce application with low-latency data access worldwide?

A: **Azure** **SQL Database**

B: **Azure** Database for MySQL

C: **Azure** **Cosmos DB**

D: **Azure** Table Storage


<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** **Cosmos DB** is designed for global distribution with turnkey replication and low-latency access from any **region**.

</details>



---

### Question 7
What is the maximum number of availability zones in a single **Azure** **region**?

A: 1

B: 2

C: 3 or more

D: Unlimited


<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** Availability **zone**-enabled regions have a minimum of 3 separate zones.

</details>



---

### Question 8
Which compute service provides the LEAST amount of management overhead?

A: Virtual Machines

B: Container Instances

C: **Azure** Functions

D: App Service


<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** **Azure** Functions is serverless - you only provide code, **Azure** manages everything else. **VMs** require the most management.

</details>



---

### Question 9
You need to transfer 500 TB of data to **Azure** but have limited network bandwidth. What should you use?

A: AzCopy

B: **Azure** Storage Explorer

C: **Azure** Data Box

D: **Azure** File Sync


<details>
<summary>✅ Show Answer</summary>

**Answer:** C

💡 **Explanation:** Data Box is a physical device for transferring massive amounts of data when network transfer isn't practical.

</details>



---

### Question 10
Which built-in **RBAC** role allows you to create and manage resources but NOT grant access to others?

A: Owner

B: Contributor

C: Reader

D: User Access Administrator


<details>
<summary>✅ Show Answer</summary>

**Answer:** B

💡 **Explanation:** Contributor can create and manage resources but cannot delegate access. Owner can do both. Reader can only view.

</details>

---

## 🎓 Next Steps

Excellent work completing Chapter 2! This was the largest section of the exam.

**Next**: Continue to [Chapter 3: **Azure** Management and Governance](03-azure-management-governance.md) to learn about cost management, governance, and monitoring.

**Review Checklist**:
- Understand all compute services and when to use each
- Memorize storage redundancy options (LRS, ZRS, GRS, GZRS)
- Know networking services (**VPN Gateway** vs **ExpressRoute**)
- Understand identity and security concepts (**RBAC**, Zero Trust, Defense in Depth)
- Be able to choose the right database for each scenario
