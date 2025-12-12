# Chapter 5: Quick Reference and Glossary

Your comprehensive reference guide for Azure terminology, service comparisons, and exam quick facts.

---

## Table of Contents
1. [Azure Services Quick Reference](#azure-services-quick-reference)
2. [Glossary of Azure Terms](#glossary-of-azure-terms)
3. [Service Comparison Tables](#service-comparison-tables)
4. [Memory Aids and Mnemonics](#memory-aids-and-mnemonics)
5. [Exam Quick Facts](#exam-quick-facts)

---

## Azure Services Quick Reference

### Compute Services

| Service | Type | Description | Use When |
|---------|------|-------------|----------|
| **Virtual Machines** | IaaS | Windows/Linux VMs in cloud | Full OS control needed, lift-and-shift |
| **VM Scale Sets** | IaaS | Autoscaling identical VMs | Variable workloads needing autoscale |
| **Availability Sets** | Feature | VMs across fault/update domains | Single datacenter high availability |
| **Availability Zones** | Feature | VMs across separate datacenters | Maximum uptime (99.99% SLA) |
| **Virtual Desktop** | DaaS | Cloud-hosted desktops | Remote work, virtual workspaces |
| **Container Instances** | CaaS | Run containers without orchestration | Simple containers, batch jobs |
| **Kubernetes Service (AKS)** | CaaS | Managed Kubernetes | Container orchestration, microservices |
| **Functions** | Serverless | Event-driven code execution | Event-driven tasks, pay per execution |
| **App Service** | PaaS | Host web apps, APIs | Web apps, focus on code not infrastructure |

### Networking Services

| Service | Type | Description | Use When |
|---------|------|-------------|----------|
| **Virtual Network (VNet)** | Core | Isolated network in Azure | Private communication between resources |
| **Network Security Group (NSG)** | Security | Firewall rules for traffic | Control inbound/outbound traffic |
| **VPN Gateway** | Hybrid | Encrypted connection over internet | Connect on-premises to Azure |
| **ExpressRoute** | Hybrid | Private dedicated connection | Mission-critical, high bandwidth, low latency |
| **Load Balancer** | Layer 4 | Distribute traffic (TCP/UDP) | Regional VM load balancing |
| **Application Gateway** | Layer 7 | HTTP/HTTPS load balancing + WAF | Web apps with advanced routing |
| **Front Door** | Layer 7 | Global load balancing + CDN | Global web apps, low latency worldwide |
| **Traffic Manager** | DNS | DNS-based routing | Global traffic distribution by routing rules |
| **Azure DNS** | DNS | Host DNS zones | Manage DNS records in Azure |

### Storage Services

| Service | Type | Description | Use When |
|---------|------|-------------|----------|
| **Blob Storage** | Object | Unstructured data (files, images, videos) | Media files, backups, data lakes |
| **File Storage** | File Share | Cloud file shares (SMB/NFS) | Replace file servers, shared access |
| **Queue Storage** | Message | Message queue | Decouple app components, async processing |
| **Table Storage** | NoSQL | Key-value NoSQL | Semi-structured data, simple queries |
| **Disk Storage** | Block | VM disks (Ultra, Premium, Standard) | Virtual machine storage |
| **Archive Storage** | Tier | Long-term cold storage | Rarely accessed data (180+ days) |

### Storage Redundancy

| Type | Copies | Location | Protects Against | Durability |
|------|--------|----------|------------------|------------|
| **LRS** | 3 | 1 datacenter | Hardware failures | 11 nines |
| **ZRS** | 3 | 3 zones (1 region) | Datacenter failure | 12 nines |
| **GRS** | 6 | 2 regions (3+3) | Regional disasters | 16 nines |
| **GZRS** | 6 | 3 zones + region | Zone + regional failures | 16 nines |
| **RA-GRS** | 6 | 2 regions (3+3) | Regional disasters + read access | 16 nines |
| **RA-GZRS** | 6 | 3 zones + region | Zone + regional + read access | 16 nines |

### Database Services

| Service | Type | Description | Use When |
|---------|------|-------------|----------|
| **SQL Database** | Relational | Managed SQL Server (PaaS) | Relational data, SQL Server apps |
| **Cosmos DB** | NoSQL | Globally distributed multi-model | Global apps, low latency, NoSQL |
| **Database for MySQL** | Relational | Managed MySQL | Open-source MySQL apps |
| **Database for PostgreSQL** | Relational | Managed PostgreSQL | Open-source PostgreSQL apps |
| **SQL Managed Instance** | Relational | Near 100% SQL Server compatibility | Lift-and-shift SQL Server |

### Identity and Security

| Service | Category | Description | Use When |
|---------|----------|-------------|----------|
| **Azure Active Directory** | Identity | Cloud identity service | User authentication, SSO |
| **Multi-Factor Authentication** | Security | 2+ factor verification | Enhanced security beyond passwords |
| **Conditional Access** | Security | Policy-based access control | Require MFA based on conditions |
| **RBAC** | Authorization | Role-based access control | Control who can do what |
| **Azure AD B2B** | Identity | Partner collaboration | External users with their credentials |
| **Azure AD B2C** | Identity | Customer identity | Consumer-facing applications |
| **Key Vault** | Security | Secret/key/certificate storage | Protect app secrets, keys, certificates |
| **Defender for Cloud** | Security | Security management + threat protection | Security recommendations, compliance |
| **Azure DDoS Protection** | Security | DDoS attack mitigation | Protect from denial of service |

### Management and Governance

| Service | Category | Description | Use When |
|---------|----------|-------------|----------|
| **Azure Portal** | Management | Web-based console | GUI management, getting started |
| **Cloud Shell** | Management | Browser-based CLI (Bash/PowerShell) | CLI without local installation |
| **Azure CLI** | Management | Cross-platform command-line | Automation, cross-platform scripts |
| **PowerShell** | Management | PowerShell cmdlets | Automation, Windows admins |
| **ARM Templates** | IaC | JSON infrastructure definitions | Infrastructure as Code, repeatability |
| **Azure Policy** | Governance | Enforce compliance rules | Ensure resource compliance |
| **Blueprints** | Governance | Package templates + policies + RBAC | Repeatable compliant environments |
| **Resource Locks** | Governance | Prevent deletion/modification | Protect critical resources |
| **Management Groups** | Organization | Organize subscriptions | Multi-subscription governance |
| **Azure Arc** | Hybrid | Manage on-premises/multi-cloud | Unified hybrid management |

### Monitoring Services

| Service | Purpose | Description | Use When |
|---------|---------|-------------|----------|
| **Azure Monitor** | Monitoring | Comprehensive monitoring platform | Collect metrics and logs |
| **Application Insights** | APM | Application performance monitoring | Monitor web app performance |
| **Log Analytics** | Analysis | Query logs with KQL | Deep log analysis, troubleshooting |
| **Azure Advisor** | Recommendations | Best practice recommendations | Improve reliability, security, performance, cost |
| **Service Health** | Health | Azure service status | Monitor Azure platform health |
| **Resource Health** | Health | Individual resource health | Check specific resource status |

### Cost Management

| Tool | Purpose | When to Use |
|------|---------|-------------|
| **Pricing Calculator** | Estimate | Before deployment - estimate costs |
| **TCO Calculator** | Compare | Compare on-premises vs Azure costs |
| **Cost Management** | Monitor | After deployment - track actual spending |
| **Budgets** | Control | Set spending limits and alerts |
| **Azure Advisor** | Optimize | Get cost reduction recommendations |

---

## Glossary of Azure Terms

### A

**Availability Set**: Logical grouping of VMs across fault and update domains within a datacenter for 99.95% SLA.

**Availability Zone**: Physically separate datacenter within an Azure region (minimum 3 zones) for 99.99% SLA.

**Azure Active Directory (Azure AD)**: Microsoft's cloud-based identity and access management service.

**Azure Arc**: Service to manage on-premises and multi-cloud resources using Azure tools.

**Azure CLI**: Cross-platform command-line tool for managing Azure (`az` commands).

**Azure Monitor**: Comprehensive monitoring solution for metrics and logs from Azure resources.

**Azure Policy**: Service to enforce rules and compliance on resource configurations.

**Azure Portal**: Web-based management console for Azure (https://portal.azure.com).

**Azure Resource Manager (ARM)**: Deployment and management layer that provides consistent API for all Azure tools.

### B

**Blob Storage**: Object storage for unstructured data (files, images, videos, backups).

**Blueprint**: Package of ARM templates, policies, and role assignments for repeatable deployments.

### C

**CapEx (Capital Expenditure)**: Upfront spending on physical infrastructure (on-premises model).

**Cloud Shell**: Browser-based command-line (Bash or PowerShell) with pre-installed Azure tools.

**Composite SLA**: Combined SLA when using multiple services (multiply individual SLAs).

**Conditional Access**: Policy-based access control based on signals (location, device, user, risk).

**Consumption-Based Model**: Pay only for what you use (OpEx model).

**Cosmos DB**: Globally distributed, multi-model NoSQL database with turnkey replication.

### D

**Defense in Depth**: Layered security approach with multiple levels of protection.

**Defender for Cloud**: Unified security management and threat protection for Azure resources.

### E

**Elasticity**: Automatic and dynamic scaling of resources based on real-time demand.

**ExpressRoute**: Private, dedicated connection between on-premises and Azure (not over internet).

### F

**Fault Domain**: Physical separation in datacenter (different racks, power, network).

**Functions**: Serverless, event-driven compute service (pay per execution).

### G

**Geo-Redundant Storage (GRS)**: Replicates data to secondary region (6 copies: 3 local + 3 remote).

### H

**Hybrid Cloud**: Combination of public cloud and private/on-premises infrastructure.

**High Availability**: Ensuring services remain accessible with minimal downtime.

### I

**IaaS (Infrastructure as a Service)**: Rent infrastructure (VMs, storage, networks). You manage OS and apps.

**Infrastructure as Code (IaC)**: Managing infrastructure through code/templates (ARM templates, Terraform).

### K

**Kubernetes Service (AKS)**: Managed Kubernetes for container orchestration.

**Kusto Query Language (KQL)**: Query language used in Log Analytics.

### L

**Load Balancer**: Layer 4 (TCP/UDP) load balancing for regional traffic distribution.

**Locally Redundant Storage (LRS)**: 3 copies in single datacenter (lowest cost redundancy).

**Log Analytics**: Tool for querying and analyzing log data using KQL.

### M

**Management Group**: Container for organizing multiple subscriptions with hierarchical governance.

**Microsoft Purview**: Unified data governance service across hybrid and multi-cloud.

**Multi-Factor Authentication (MFA)**: Authentication requiring 2+ verification factors.

### N

**Network Security Group (NSG)**: Firewall rules controlling inbound/outbound traffic to resources.

### O

**OpEx (Operational Expenditure)**: Ongoing costs for services (cloud model).

### P

**PaaS (Platform as a Service)**: Managed platform for deploying apps. You manage apps and data.

**Passwordless Authentication**: Authentication without passwords (Windows Hello, FIDO2, Authenticator).

**Pay-as-you-go**: Pricing model where you pay based on actual usage.

**Pricing Calculator**: Tool to estimate Azure costs before deployment.

**Private Cloud**: Cloud environment dedicated to one organization.

**Public Cloud**: Cloud resources owned by provider, shared among multiple customers.

### R

**RBAC (Role-Based Access Control)**: Authorization system controlling who can perform actions on resources.

**Region**: Geographical area with one or more datacenters (Azure has 60+ regions).

**Region Pair**: Two regions paired for disaster recovery (300+ miles apart, same geography).

**Reliability**: Ability to recover from failures and continue functioning.

**Reserved Instance**: Commitment to 1-3 years for VMs/databases for up to 72% discount.

**Resource**: Manageable item in Azure (VM, storage account, database, etc.).

**Resource Group**: Logical container for grouping related resources.

**Resource Lock**: Prevents deletion (CanNotDelete) or modification (ReadOnly) of resources.

### S

**SaaS (Software as a Service)**: Complete software delivered over internet (Microsoft 365, Teams).

**Scalability**: Ability to increase or decrease resources (vertical or horizontal).

**Service Health**: Personalized view of Azure service status affecting your resources.

**Shared Responsibility Model**: Defines security/operational tasks split between provider and customer.

**Single Sign-On (SSO)**: Sign in once to access multiple applications.

**SLA (Service Level Agreement)**: Microsoft's commitment to service availability (e.g., 99.9%).

**Sovereign Region**: Isolated Azure instance for specific government/compliance (Azure Government, Azure China).

**Spot VM**: Use spare capacity at steep discounts (can be evicted).

**Subscription**: Logical unit for billing and access control, linked to Azure account.

### T

**Table Storage**: NoSQL key-value store for semi-structured data.

**Tag**: Name-value pair for organizing resources (e.g., Environment:Production).

**TCO Calculator**: Total Cost of Ownership calculator comparing on-premises vs Azure.

**Traffic Manager**: DNS-based global traffic routing.

### U

**Update Domain**: Logical separation for planned maintenance updates.

### V

**Virtual Machine (VM)**: IaaS compute service providing virtualized Windows/Linux servers.

**Virtual Network (VNet)**: Isolated network in Azure for private resource communication.

**VPN Gateway**: Sends encrypted traffic between Azure and on-premises over internet.

### Z

**Zero Trust**: Security model: "Never trust, always verify" - assume breach, verify every request.

**Zone-Redundant Storage (ZRS)**: 3 copies across 3 availability zones in same region.

---

## Service Comparison Tables

### IaaS vs PaaS vs SaaS

| Aspect | IaaS | PaaS | SaaS |
|--------|------|------|------|
| **Examples** | Azure VMs, Storage | App Service, SQL Database | Microsoft 365, Dynamics 365 |
| **You Manage** | OS, middleware, apps, data | Apps and data | Data and access |
| **Provider Manages** | Physical infrastructure | Infrastructure + platform | Everything except your data |
| **Control** | Maximum | Medium | Minimum |
| **Flexibility** | Highest | Medium | Lowest |
| **Setup Time** | Longer | Medium | Fastest |
| **Technical Knowledge** | High | Medium | Low |
| **Use Case** | Custom apps, full control | App development | Ready-to-use software |

### Cloud Deployment Models

| Model | Ownership | Location | Pros | Cons | Use Case |
|-------|-----------|----------|------|------|----------|
| **Public** | Provider | Provider datacenter | Low cost, no maintenance, high scale | Less control, shared resources | General workloads, startups |
| **Private** | Organization | On-premises or hosted | Full control, enhanced security | High cost, limited scale | Regulatory compliance, sensitive data |
| **Hybrid** | Mixed | Both | Flexibility, gradual migration | Complexity, networking costs | Partial migration, mixed requirements |

### VPN Gateway vs ExpressRoute

| Feature | VPN Gateway | ExpressRoute |
|---------|-------------|--------------|
| **Connection** | Over internet (encrypted) | Private dedicated line |
| **Speed** | Up to 10 Gbps | Up to 100 Gbps |
| **Latency** | Higher (internet routing) | Lower (dedicated path) |
| **Reliability** | Depends on internet | Very high (dedicated) |
| **Security** | Encrypted over internet | Private (doesn't traverse internet) |
| **Cost** | Lower | Higher |
| **Setup Time** | Faster | Longer (provisioning) |
| **Best For** | SMB, dev/test, lower budgets | Enterprise, mission-critical, high bandwidth |

### Load Balancing Services

| Service | Layer | Scope | Protocol | Best For |
|---------|-------|-------|----------|----------|
| **Load Balancer** | 4 (Transport) | Regional | TCP/UDP | VM load balancing in region |
| **Application Gateway** | 7 (Application) | Regional | HTTP/HTTPS | Web apps with WAF, URL routing |
| **Front Door** | 7 (Application) | Global | HTTP/HTTPS | Global web apps, CDN, WAF |
| **Traffic Manager** | DNS | Global | DNS | DNS-based global routing |

### Storage Redundancy Options

| Type | Copies | Where | Protects Against | Read Access to Secondary | Cost |
|------|--------|-------|------------------|--------------------------|------|
| **LRS** | 3 | 1 datacenter | Hardware failure | No | Lowest |
| **ZRS** | 3 | 3 zones | Datacenter failure | No | Low |
| **GRS** | 6 | 2 regions | Regional disaster | No (unless RA-GRS) | Medium |
| **GZRS** | 6 | 3 zones + region | Zone + regional | No (unless RA-GZRS) | Highest |

### Azure Policy vs RBAC vs Locks

| Feature | Azure Policy | RBAC | Resource Locks |
|---------|-------------|------|----------------|
| **Purpose** | Enforce compliance | Control access | Prevent changes |
| **Focuses On** | WHAT (resource properties) | WHO (user permissions) | PREVENT (deletion/modification) |
| **Scope** | Resource configurations | User actions | Resource protection |
| **Example** | "VMs must use managed disks" | "User can read VMs" | "Cannot delete production DB" |
| **Override** | Can audit or deny | Based on role hierarchy | Overrides all permissions |

### Monitoring Services Comparison

| Service | What It Does | When to Use |
|---------|--------------|-------------|
| **Azure Advisor** | Best practice recommendations | Get personalized improvement suggestions |
| **Service Health** | Azure platform status | Check Azure service incidents/maintenance |
| **Azure Monitor** | Collect metrics and logs | Comprehensive resource monitoring |
| **Application Insights** | Application performance | Monitor web app performance and usage |
| **Log Analytics** | Query and analyze logs | Deep troubleshooting, log analysis |

### Database Services Comparison

| Service | Type | Model | Best For | Global Distribution |
|---------|------|-------|----------|---------------------|
| **SQL Database** | Relational | Single-model | Relational data, SQL Server apps | Manual (geo-replication) |
| **Cosmos DB** | NoSQL | Multi-model | Global apps, low latency, flexible schema | Turnkey (built-in) |
| **MySQL** | Relational | Single-model | Open-source MySQL apps | Manual |
| **PostgreSQL** | Relational | Single-model | Open-source PostgreSQL apps | Manual |

---

## Memory Aids and Mnemonics

### Service Models: IaaS, PaaS, SaaS

**Pizza as a Service Analogy**:
- **On-Premises**: You make everything (buy ingredients, make dough, cook, serve, clean)
- **IaaS**: Take and bake (you get oven and kitchen, you cook and serve)
- **PaaS**: Pizza delivery (they make it, you eat it at home)
- **SaaS**: Dine in restaurant (they make, serve, and clean up)

### Shared Responsibility Model

**Remember**: "You ALWAYS own your DATA, DEVICES, and ACCOUNTS"
- No matter what service model, you're responsible for:
  - **D**ata
  - **D**evices
  - **A**ccounts

**Provider ALWAYS owns**: "Physical stuff you can touch"
- **P**hysical datacenter
- **P**hysical network
- **P**hysical hosts

### Storage Redundancy (LRS, ZRS, GRS, GZRS)

**"Layers of Protection"**:
- **L**RS = **L**ocal (1 datacenter) = **L**owest protection
- **Z**RS = **Z**ones (3 zones) = **Z**one protection
- **G**RS = **G**eographic (2 regions) = **G**lobal protection
- **GZRS** = **G**eographic + **Z**ones = **G**reatest protection

**Copies**: "3, 3, 6, 6" (LRS=3, ZRS=3, GRS=6, GZRS=6)

### SLA Downtime

**The "Nines Rule"**:
- 99% = "2 nines" = ~3.65 days/year = "Too much for production"
- 99.9% = "3 nines" = ~8.7 hours/year = "Basic production"
- 99.95% = "almost 4 nines" = ~4.4 hours/year = "Good production"
- 99.99% = "4 nines" = ~52 minutes/year = "Mission-critical"
- 99.999% = "5 nines" = ~5 minutes/year = "Exceptional"

**Remember**: Each nine reduces downtime by ~10x

### Azure Policy vs RBAC

**"WHO vs WHAT"**:
- **RBAC** = **WHO** can do actions
- **Policy** = **WHAT** configurations are allowed

**Example**:
- RBAC: "Bob CAN create VMs"
- Policy: "VMs MUST be in West US region"

### Support Plans

**"The Money Pyramid"**:
```
        Premier (Custom $$$$$)
      Professional Direct ($1000)
         Standard ($100)
        Developer ($29)
       Basic (FREE)
```

**Critical Response Times**: "None, None, 1, 1, 15"
- Basic: No technical support
- Developer: No critical support
- Standard: <1 hour
- Professional Direct: <1 hour (prioritized)
- Premier: <15 minutes

### Availability Options for VMs

**"Set, Zone, Pair"**:
- **Availability Set** = Within datacenter = 99.95% SLA
- **Availability Zones** = Across datacenters = 99.99% SLA
- **Region Pairs** = Across regions = Disaster recovery (no SLA number)

### Cost Management Tools

**"Before, Compare, After"**:
- **Before** deployment = **Pricing Calculator**
- **Compare** on-prem vs Azure = **TCO Calculator**
- **After** deployment = **Cost Management**

### Command-Line Tools

**Format Recognition**:
- **PowerShell**: `Verb-AzNoun` → "Get**-Az**VM"
- **CLI**: `az group command` → "**az** vm list"

---

## Exam Quick Facts

### SLA Reference

| SLA % | Downtime/Month | Downtime/Year | Service Example |
|-------|----------------|---------------|-----------------|
| 99% | 7.2 hours | 3.65 days | Not common in Azure |
| 99.9% | 43.2 minutes | 8.7 hours | Single VM (Premium SSD) |
| 99.95% | 21.6 minutes | 4.4 hours | VMs in Availability Set |
| 99.99% | 4.3 minutes | 52.6 minutes | VMs across Zones, SQL DB |
| 99.999% | 26 seconds | 5.3 minutes | Cosmos DB (multi-region) |

### Storage Redundancy Quick Facts

- **LRS**: 3 copies, 1 datacenter, 11 nines durability
- **ZRS**: 3 copies, 3 zones, 12 nines durability
- **GRS**: 6 copies (3+3), 2 regions, 16 nines durability
- **GZRS**: 6 copies (3 zones + 3 remote), 16 nines durability
- **RA-GRS/RA-GZRS**: Same as GRS/GZRS + read access to secondary

### Availability Zones Facts

- **Minimum**: 3 zones per enabled region
- **Distance**: Physically separate datacenters
- **Connection**: High-speed private fiber
- **SLA**: 99.99% for VMs across zones
- **Not all regions**: Support availability zones

### Region Pairs Facts

- **Distance**: Minimum 300 miles apart
- **Geography**: Always in same geography (for compliance)
- **Updates**: Only one region updated at a time
- **Replication**: Some services auto-replicate to pair
- **Purpose**: Disaster recovery and business continuity

### Support Plan Quick Reference

| Plan | Cost | Technical Support | Critical Response | Best For |
|------|------|-------------------|-------------------|----------|
| **Basic** | Free | None | N/A | Billing questions only |
| **Developer** | $29/mo | Email (business hours) | N/A | Non-production |
| **Standard** | $100/mo | 24/7 email/phone | <1 hour | Production workloads |
| **Professional Direct** | $1,000/mo | 24/7 email/phone | <1 hour (priority) | Business-critical |
| **Premier** | Custom | 24/7 email/phone | <15 min | Large enterprises |

### Resource Hierarchy

```
Management Group
  └── Subscription
      └── Resource Group
          └── Resource
```

- Management groups organize multiple subscriptions
- Subscriptions are billing/access boundaries
- Resource groups are logical containers
- Resources are actual services (VMs, storage, etc.)

### Virtual Machine SLAs

| Configuration | SLA | Use Case |
|---------------|-----|----------|
| Single VM (Premium SSD) | 99.9% | Single instance workloads |
| Availability Set | 99.95% | Protection within datacenter |
| Availability Zones | 99.99% | Protection across datacenters |

### Composite SLA Calculation

**Formula**: SLA₁ × SLA₂ × SLA₃...

**Example**:
- App Service: 99.95%
- SQL Database: 99.99%
- Composite: 99.95% × 99.99% = **99.94%**

**Key Point**: Adding dependencies LOWERS overall SLA

### Data Transfer Costs

- **Inbound** (to Azure): FREE
- **Outbound** (from Azure): CHARGED (data egress)
- **Between regions**: CHARGED
- **Within region**: Often free or low cost

### Tags

- **Maximum**: 50 tags per resource
- **Name**: Up to 512 characters
- **Value**: Up to 256 characters
- **Purpose**: Organization, cost tracking, automation
- **Not all resources**: Support tags

### Management Tools Summary

| Tool | Interface | Best For |
|------|-----------|----------|
| **Portal** | GUI (web) | Visual management, getting started |
| **Cloud Shell** | Browser CLI | Quick CLI access, any device |
| **CLI** | Command-line | Cross-platform automation, Linux |
| **PowerShell** | Cmdlets | Windows automation, scripting |
| **ARM Templates** | JSON | Infrastructure as Code |
| **Mobile App** | Mobile GUI | Monitoring on the go |

### Key Port Numbers (Sometimes on Exam)

- **HTTP**: 80
- **HTTPS**: 443
- **RDP** (Remote Desktop): 3389
- **SSH**: 22
- **SQL Server**: 1433
- **MySQL**: 3306
- **PostgreSQL**: 5432

### Resource Lock Types

| Lock Type | Can Read | Can Modify | Can Delete |
|-----------|----------|------------|------------|
| **CanNotDelete** | Yes | Yes | No |
| **ReadOnly** | Yes | No | No |
| **No Lock** | Yes | Yes | Yes |

---

## Final Exam Preparation Checklist

### Core Concepts to Know Cold

**Cloud Concepts**:
- ✓ IaaS vs PaaS vs SaaS with examples
- ✓ Public vs Private vs Hybrid cloud
- ✓ Shared Responsibility Model
- ✓ CapEx vs OpEx
- ✓ Consumption-based model

**Azure Architecture**:
- ✓ Regions, Availability Zones, Region Pairs
- ✓ Storage redundancy (LRS, ZRS, GRS, GZRS)
- ✓ Compute services (VMs, App Service, Functions, Containers)
- ✓ Networking (VNet, NSG, VPN, ExpressRoute)
- ✓ Database options (SQL, Cosmos DB, MySQL, PostgreSQL)

**Identity & Security**:
- ✓ Azure AD, SSO, MFA, Passwordless
- ✓ RBAC, Conditional Access
- ✓ Zero Trust, Defense in Depth
- ✓ Defender for Cloud

**Management & Governance**:
- ✓ Cost tools (Pricing Calc, TCO, Cost Management)
- ✓ Azure Policy vs RBAC vs Locks
- ✓ ARM, ARM Templates, IaC
- ✓ Monitoring services (Advisor, Monitor, Service Health)
- ✓ Support plans

**SLAs**:
- ✓ Common SLA percentages
- ✓ Composite SLA calculation
- ✓ VM SLA configurations

### Day Before Exam

- [ ] Review all practice questions (Chapter 4)
- [ ] Review this glossary and quick reference
- [ ] Review chapter summaries
- [ ] Create free Azure account if not done (hands-on helps)
- [ ] Get good sleep
- [ ] Prepare ID and exam confirmation

### Exam Day Reminders

- Read questions carefully (look for keywords)
- Eliminate obviously wrong answers
- Don't overthink (fundamentals exam)
- Mark uncertain questions for review
- Use all 60 minutes
- No penalty for guessing (answer everything)

---

## Congratulations!

You've completed the comprehensive AZ-900 study guide!

**You now have**:
- ✓ Deep understanding of cloud concepts
- ✓ Knowledge of Azure architecture and services
- ✓ Understanding of management and governance
- ✓ 75+ practice questions with explanations
- ✓ Quick reference materials and memory aids

**Next Steps**:
1. Take official Microsoft practice assessment
2. Review any weak areas
3. Practice with Azure Portal (hands-on)
4. Schedule your exam when ready
5. Pass and get certified!

**Resources**:
- Microsoft Learn: https://learn.microsoft.com/certifications/azure-fundamentals/
- Azure Portal: https://portal.azure.com
- Free Azure Account: https://azure.microsoft.com/free/

**You're well-prepared. Good luck on your AZ-900 exam!**
