# 📙 Chapter 3: Azure Management and Governance

> **📊 Exam Weight:** 30-35% of total exam
> **⏱️ Estimated Time:** 3-4 hours
> **📝 Practice Questions:** 15 questions at end of chapter
> **🎯 Learning Objective:** Master cost management, governance, and monitoring

---

## 📖 Chapter Overview

This chapter covers cost management, governance, resource management tools, and monitoring - critical topics for the AZ-900 exam.

**What You'll Learn:**
- 💰 Cost management and optimization strategies
- 📊 Azure pricing and TCO calculators
- 🛡️ Governance tools (Policy, Blueprints, Locks)
- ⚙️ Resource management (Portal, CLI, PowerShell, ARM)
- 📈 Monitoring services (Advisor, Monitor, Service Health)
- 📋 SLAs and support plans


---

## Table of Contents
1. [Cost Management in **Azure**](#cost-management-in-azure)
2. [**Azure** Governance and Compliance](#azure-governance-and-compliance)
3. [Resource Management Tools](#resource-management-tools)
4. [Monitoring and Management](#monitoring-and-management)
5. [Service Level Agreements (SLAs)](#service-level-agreements-slas)
6. [**Azure** Support Plans](#azure-support-plans)
7. [Chapter Summary](#chapter-summary)
8. [Practice Questions](#practice-questions)


---

## Cost Management in **Azure**

Understanding **Azure** costs and how to optimize them is crucial for the exam.

### Factors Affecting Costs

**1. Resource Type**
- Different services have different pricing models
- Example: **VMs** priced by size, **region**, OS; Storage by capacity and operations

**2. Consumption**
- **Pay-as-you-go**: Charged based on actual usage
- Many services billed per second, minute, or hour
- Some services have flat rates or tiers

**3. Maintenance**
- Maintaining resources properly can reduce costs
- Stop/deallocate **VMs** when not in use
- Right-size resources to match needs
- Remove unused resources

**4. Geography/Region**
- Prices vary by **Azure** **region**
- Same service can cost more in certain regions
- Data transfer between regions incurs charges
- Consider deploying closer to users in cost-effective regions

**5. Network Traffic**
- **Inbound data**: Usually free
- **Outbound data**: Often charged (data egress)
- **Between regions**: Charged for data transfer
- **Within same region**: Often free or lower cost

**6. Subscription Type**
- Free tier: Limited free services
- Pay-as-you-go: Standard rates
- Enterprise Agreement: Volume discounts
- Dev/Test: Discounted rates for development

**7. **Azure** Marketplace**
- Third-party solutions may have additional costs
- Combined billing through **Azure**

> **💡 EXAM TIP:** Know that **region**, resource type, and consumption are the main cost factors. Outbound data transfer is charged.

### Pricing Calculator

**What It Is**: Web-based tool to estimate costs for **Azure** services BEFORE you deploy them.

**How to Use**:
1. Add services you plan to use
2. Configure service options (size, **region**, tier)
3. View estimated monthly costs
4. Save and share estimates

**Features**:
- Estimate costs for any **Azure** service
- Compare different configurations
- Export estimates
- No **Azure** account required

**📋 Common Use Cases:**
- Planning new **Azure** deployments
- Comparing costs between regions
- Budget planning
- Cost comparison for different architectures

**URL**: https://azure.microsoft.com/pricing/calculator/

> **💡 EXAM TIP:** Pricing Calculator is for ESTIMATING costs BEFORE deployment. Use Cost Management for ACTUAL costs after deployment.

### Total Cost of Ownership (TCO) Calculator

**What It Is**: Tool to compare costs of running on-premises infrastructure versus **Azure**.

**What It Calculates**:
- Current on-premises costs:
  - Servers (hardware, software, facilities, labor)
  - Databases
  - Storage
  - Networking
  - Datacenter costs (power, cooling, maintenance)
  - IT labor
- Projected **Azure** costs for same workloads
- Cost savings over time (typically 3-5 years)

**How to Use**:
1. Define your current on-premises workloads
2. Enter assumptions (electricity costs, IT labor rates, etc.)
3. View side-by-side comparison
4. Adjust assumptions and scenarios

**✅ Benefits:**
- Justifies cloud migration to stakeholders
- Reveals hidden on-premises costs
- Shows long-term savings
- Helps with budgeting and planning

**URL**: https://azure.microsoft.com/pricing/tco/calculator/

> **💡 EXAM TIP:** TCO Calculator compares on-premises vs **Azure** costs to justify migration. Pricing Calculator estimates **Azure**-only costs.

### Cost Management and Billing

**What It Is**: Suite of tools to monitor, allocate, and optimize **Azure** spending.

**Key Features**:

**Cost Analysis**:
- View current spending
- Break down by resource, resource group, **subscription**
- Historical trends
- Forecast future costs

**Budgets**:
- Set spending limits
- Create alerts at thresholds (50%, 80%, 100%)
- Monthly, quarterly, or annual budgets
- Email notifications when exceeded

**Recommendations**:
- Identify idle resources
- Suggest right-sizing opportunities
- Recommend reserved instances
- Spot unused resources

**Exports**:
- Schedule automatic cost data exports
- Export to storage account
- Integrate with external tools

**Cost Allocation**:
- Use tags to organize costs
- Track spending by department, project, environment
- Chargeback and showback reporting

> **💡 EXAM TIP:** Cost Management helps you monitor, analyze, and optimize actual spending. Available in **Azure** Portal.

### Cost Optimization Strategies

**1. Reserved Instances**
- Commit to 1 or 3 years for **VMs**, **SQL Database**, **Cosmos DB**, etc.
- Save up to 72% compared to pay-as-you-go
- Pay monthly or upfront
- Can exchange or cancel with restrictions

**2. **Azure** Hybrid Benefit**
- Use existing Windows Server and SQL Server licenses in **Azure**
- Save up to 40% on **VMs**
- Save up to 55% on **SQL Database**
- Requires Software Assurance

**3. Spot VMs**
- Use spare **Azure** capacity at steep discounts (up to 90%)
- Can be evicted when **Azure** needs capacity
- Good for: Batch jobs, dev/test, interruptible workloads

**4. Right-Sizing**
- Match **VM** size to actual workload requirements
- Monitor utilization and downsize underutilized **VMs**
- Cost Management provides recommendations

**5. Auto-Shutdown**
- Schedule **VMs** to shut down during non-business hours
- Available in **Azure** Portal for **VMs**
- Saves costs on compute (storage still charged)

**6. Deallocate vs Stop**
- **Stop**: **VM** still allocated, still charged
- **Deallocate**: Release compute resources, no compute charges
- Always deallocate to stop charges

**7. Serverless**
- Use **Azure** Functions, Logic Apps for event-driven workloads
- Pay only when code executes
- Automatic scaling included

**8. Storage Optimization**
- Use appropriate access tier (Hot, Cool, Archive)
- Enable lifecycle management to move data between tiers
- Delete unused snapshots and disks

**9. Use Tags**
- Tag resources by environment, department, project
- Track and allocate costs accurately
- Implement chargeback models

> **💡 EXAM TIP:** Know all optimization strategies. Common exam questions ask how to reduce costs in specific scenarios.

### Resource Tagging

**What It Is**: Name-value pairs applied to **Azure** resources for organization and cost tracking.

**Format**: `Name: Value`
- Example: `Environment: Production`
- Example: `Department: Finance`
- Example: `Project: Migration`

**📋 Common Use Cases:**
- **Cost tracking**: View spending by department or project
- **Resource organization**: Group related resources
- **Automation**: Apply policies based on tags
- **Access control**: Grant access based on tags

**Best Practices**:
- Develop tagging strategy before deployment
- Enforce required tags with **Azure** Policy
- Use consistent naming conventions
- Document tag meanings

**Limitations**:
- Maximum 50 tags per resource
- Tag names: up to 512 characters
- Tag values: up to 256 characters
- Not all resources support tags

> **💡 EXAM TIP:** Tags are for organization and cost allocation. They don't provide access control directly (use **RBAC** for that).


---

## **Azure** Governance and Compliance

### Microsoft Purview

**What It Is**: Unified data governance service for managing and governing on-premises, multi-cloud, and **SaaS** data.

**Key Features**:
- **Data discovery**: Automatically scan and classify data
- **Data catalog**: Searchable inventory of data assets
- **Data lineage**: Track data from source to destination
- **Sensitivity labeling**: Classify and protect sensitive data
- **Compliance reporting**: Meet regulatory requirements

**Components**:
- **Data Map**: Automated data discovery and classification
- **Data Catalog**: Find and understand data assets
- **Data Estate Insights**: Reports on data estate health

**📋 Common Use Cases:**
- Data discovery across hybrid and multi-cloud
- Regulatory compliance (GDPR, HIPAA)
- Data loss prevention
- Data lifecycle management

> **💡 EXAM TIP:** Purview is for data governance - discovering, classifying, and managing data across your entire estate.

### **Azure** Policy

**What It Is**: Service to create, assign, and manage policies that enforce rules and ensure resource compliance.

**How It Works**:
1. Create or use built-in policy definitions
2. Assign policies to scope (management group, **subscription**, resource group)
3. **Azure** evaluates resources for compliance
4. View compliance results and remediate non-compliant resources

**Common Policy Examples**:
- Allowed virtual machine sizes
- Allowed locations for resources
- Require tag on resources
- Enforce encryption on storage accounts
- Require backup on **VMs**
- Audit **VMs** without managed disks

**Policy vs RBAC**:
- **RBAC**: Controls WHO can perform actions
- **Policy**: Controls WHAT actions can be performed and resource configurations

**Effects**:
- **Deny**: Prevent resource creation/update
- **Audit**: Log non-compliant resources (no action)
- **Append**: Add properties to resources
- **Modify**: Add, update, or remove properties
- **DeployIfNotExists**: Deploy resources if they don't exist

**✅ Benefits:**
- Enforce organizational standards
- Ensure compliance at scale
- Prevent deployment of non-compliant resources
- Audit existing resources

> **💡 EXAM TIP:** **Azure** Policy enforces rules and compliance. Focuses on resource properties and compliance standards.

### **Azure** Blueprints

**What It Is**: Declarative way to orchestrate deployment of resource templates, policies, role assignments, and resource groups.

**Components**:
- Resource groups
- ARM templates
- Policy assignments
- Role assignments

**How It Differs from ARM Templates**:
- **ARM Templates**: Deploy resources
- **Blueprints**: Package ARM templates + policies + **RBAC** + resource groups together
- Blueprints maintain relationship between definition and assignment
- Versioning and tracking

**📋 Common Use Cases:**
- Rapidly build and deploy compliant environments
- Ensure governance policies applied to new subscriptions
- Audit and track deployments
- Repeatable environment setup

**Lifecycle**:
1. Create blueprint definition
2. Assign blueprint to **subscription**
3. Track and audit deployments
4. Update blueprint versions

> **💡 EXAM TIP:** Blueprints = package of ARM templates + policies + **RBAC** for repeatable, compliant environment deployment.

### Resource Locks

**What It Is**: Mechanism to prevent accidental deletion or modification of critical resources.

**Lock Types**:

**CanNotDelete** (Delete lock):
- Can read and modify resource
- Cannot delete resource
- Use case: Prevent accidental deletion of production databases

**ReadOnly**:
- Can only read resource
- Cannot modify or delete
- Use case: Production resources that should never change

**Lock Behavior**:
- Applied to resource, resource group, or **subscription**
- Child resources inherit locks
- Locks apply to ALL users, regardless of **RBAC** permissions
- Must remove lock before performing blocked action

**Who Can Create/Delete Locks**:
- Owner and User Access Administrator roles
- Custom roles with `Microsoft.Authorization/*` or `Microsoft.Authorization/locks/*`

> **💡 EXAM TIP:** Resource locks prevent deletion (CanNotDelete) or changes (ReadOnly). Locks override **RBAC** permissions.


---

## Resource Management Tools

**Azure** provides multiple ways to manage resources - know when to use each.

### **Azure** Portal

**What It Is**: Web-based management console for **Azure** (https://portal.azure.com).

**Features**:
- Graphical user interface (GUI)
- Create and manage all **Azure** resources
- Customizable dashboards
- **Azure** Cloud Shell integration
- Mobile-friendly (responsive design)
- Accessible from any browser

**Best For**:
- Getting started with **Azure**
- Visual management and monitoring
- One-time or infrequent tasks
- Exploring **Azure** services
- Users who prefer GUI over CLI

**Characteristics**:
- Always up-to-date (no installation)
- Built-in resilience (available even during **Azure** outages)
- Accessible from anywhere

> **💡 EXAM TIP:** Portal is the GUI-based management tool, accessible via web browser.

### **Azure** Cloud Shell

**What It Is**: Browser-based shell environment accessible from **Azure** Portal.

**Features**:
- Choice of Bash or PowerShell
- Pre-installed tools (**Azure** CLI, PowerShell, Terraform, Ansible, etc.)
- Authenticated automatically to your **Azure** account
- Persistent storage (5 GB included free)
- Access files between sessions
- Available in **Azure** Portal or https://shell.azure.com

**✅ Benefits:**
- No local installation required
- Works from any device with browser
- Always up-to-date tools
- Secure (authenticated automatically)

**📋 Common Use Cases:**
- Quick **Azure** management tasks
- Running scripts without local setup
- Managing **Azure** from mobile devices
- Learning **Azure** CLI/PowerShell

> **💡 EXAM TIP:** Cloud Shell = browser-based command line (Bash or PowerShell) with pre-installed **Azure** tools.

### **Azure** PowerShell

**What It Is**: PowerShell module for managing **Azure** resources via cmdlets.

**Characteristics**:
- PowerShell cmdlets (commands)
- Cmdlet format: `Verb-AzNoun` (e.g., `Get-AzVM`, `New-AzResourceGroup`)
- Cross-platform (Windows, Linux, macOS)
- Can be installed locally or used in Cloud Shell
- Scripting and automation

**Common Cmdlets**:
- `Connect-AzAccount`: Sign in to **Azure**
- `Get-AzVM`: List virtual machines
- `New-AzResourceGroup`: Create resource group
- `Remove-AzResourceGroup`: Delete resource group

**Best For**:
- Windows administrators familiar with PowerShell
- Automation and scripting
- Bulk operations
- Integration with existing PowerShell scripts

> **💡 EXAM TIP:** **Azure** PowerShell = PowerShell cmdlets for **Azure**, format: Verb-AzNoun.

### **Azure** CLI

**What It Is**: Cross-platform command-line tool for managing **Azure** resources.

**Characteristics**:
- Command format: `az <group> <command>` (e.g., `az vm list`, `az group create`)
- JSON output by default
- Cross-platform (Windows, Linux, macOS)
- Can be installed locally or used in Cloud Shell
- Scripting and automation

**Common Commands**:
- `az login`: Sign in to **Azure**
- `az vm list`: List virtual machines
- `az group create`: Create resource group
- `az group delete`: Delete resource group

**Best For**:
- Linux administrators
- Cross-platform scripting
- Automation and CI/CD pipelines
- Users who prefer Unix-like command syntax

**PowerShell vs CLI**:

| Feature | **Azure** PowerShell | **Azure** CLI |
|---------|------------------|-----------|
| **Format** | Verb-AzNoun cmdlets | az group command |
| **Output** | Objects | JSON (default) |
| **Best For** | PowerShell users, Windows | Cross-platform, Linux |
| **Platform** | Cross-platform | Cross-platform |

> **💡 EXAM TIP:** **Azure** CLI = cross-platform command-line tool, commands start with 'az'.

### **Azure** Mobile App

**What It Is**: Mobile application for monitoring and managing **Azure** resources on iOS and Android.

**Features**:
- Monitor resource health and status
- View alerts and notifications
- Start/stop **VMs**
- Run **Azure** CLI commands via Cloud Shell
- Respond to alerts quickly

**📋 Common Use Cases:**
- On-the-go monitoring
- Responding to alerts when away from desk
- Quick status checks
- Emergency resource management

**Limitations**:
- Limited compared to full Portal
- Best for monitoring and simple tasks
- Complex operations better suited for Portal/CLI/PowerShell

> **💡 EXAM TIP:** **Azure** Mobile App allows basic monitoring and management from mobile devices.

### **Azure** Resource Manager (ARM)

**What It Is**: Deployment and management layer for **Azure**, provides consistent management interface.

**All **Azure** Interactions Go Through ARM**:
```
Portal, CLI, PowerShell, SDKs → ARM → **Azure** Resources
```

**✅ Benefits:**
- **Consistent interface**: All tools use same API
- **Declarative templates**: Define infrastructure as code
- **Dependency management**: Deploy resources in correct order
- **Access control**: **RBAC** integrated at all levels
- **Tagging**: Organize resources logically
- **Billing**: Track costs by tags and groups

**ARM Templates**:
- JSON files defining **Azure** resources
- Infrastructure as Code (IaC)
- Repeatable deployments
- Version control friendly
- Modular and reusable

**Template Sections**:
- `parameters`: Input values
- `variables`: Reusable values
- `resources`: Resources to deploy
- `outputs`: Return values after deployment

**Benefits of Templates**:
- Consistent deployments
- Reduce human error
- Version control infrastructure
- Deploy complex environments quickly
- Reuse across environments (dev, test, prod)

> **💡 EXAM TIP:** ARM is the deployment layer ALL **Azure** tools use. ARM Templates enable Infrastructure as Code.

### **Azure** Arc

**What It Is**: Extends **Azure** management and services to any infrastructure (on-premises, multi-cloud, edge).

**What You Can Manage**:
- **Servers**: Windows and Linux machines anywhere
- **Kubernetes clusters**: On-premises or other clouds
- ****Azure** data services**: SQL Managed Instance, PostgreSQL anywhere
- **SQL Servers**: Inventory and manage SQL Servers anywhere

**✅ Benefits:**
- Unified management across environments
- Apply **Azure** policies anywhere
- Use **Azure** **RBAC** for on-premises resources
- Monitor with **Azure** Monitor
- Consistent governance across hybrid infrastructure

**📋 Common Use Cases:**
- Manage on-premises servers from **Azure**
- Multi-cloud management (AWS, GCP, **Azure**)
- Apply **Azure** governance to non-**Azure** resources
- Gradual cloud migration

> **💡 EXAM TIP:** **Azure** Arc brings **Azure** management to on-premises and multi-cloud resources.

### Infrastructure as Code (IaC)

**Concept**: Manage infrastructure through code and templates rather than manual processes.

**✅ Benefits:**
- **Consistency**: Same code = same result every time
- **Repeatability**: Deploy identical environments easily
- **Version control**: Track changes to infrastructure
- **Automation**: Integrate with CI/CD pipelines
- **Documentation**: Code serves as documentation
- **Faster deployment**: Automated vs manual

****Azure** IaC Tools**:
- **ARM Templates**: **Azure**-native JSON templates
- **Bicep**: Simplified ARM template language
- **Terraform**: Multi-cloud IaC tool
- **Ansible**: Configuration management and deployment

> **💡 EXAM TIP:** IaC allows managing infrastructure through code for consistency, automation, and version control.


---

## Monitoring and Management

### **Azure** Advisor

**What It Is**: Personalized cloud consultant that provides best practice recommendations.

**Recommendation Categories**:

**1. Reliability** (formerly High Availability):
- Enable backups
- Use availability zones
- Configure disaster recovery
- Remove single points of failure

**2. Security**:
- Enable **MFA**
- Restrict network access
- Enable encryption
- Update security agents

**3. Performance**:
- Upgrade to faster disks
- Scale **VMs** appropriately
- Optimize database performance
- Use CDN for better performance

**4. Cost**:
- Right-size underutilized **VMs**
- Delete unused resources
- Purchase reserved instances
- Use appropriate storage tiers

**5. Operational Excellence**:
- Follow best practices for resource organization
- Improve resource health
- Optimize **subscription** limits
- Implement proper tagging

**How It Works**:
- Analyzes resource configuration and usage
- Generates personalized recommendations
- Prioritizes recommendations by impact
- Free service (no cost)

> **💡 EXAM TIP:** Advisor provides FREE recommendations across 5 categories: Reliability, Security, Performance, Cost, Operational Excellence.

### **Azure** Service Health

**What It Is**: Personalized view of **Azure** service health and planned maintenance affecting your resources.

**Components**:

****Azure** Status**:
- Global view of all **Azure** services across all regions
- Public status page (https://status.azure.com)
- Anyone can view (no login required)

**Service Health**:
- Personalized view of services and regions YOU use
- Current issues affecting your resources
- Upcoming planned maintenance
- Health advisories

**Resource Health**:
- Health of individual resources (**VMs**, databases, etc.)
- Current and historical health status
- Reason for health issues
- Troubleshooting steps

**Health Alerts**:
- Configure alerts for service issues
- Email, SMS, webhook notifications
- Action groups for automated responses
- Stay informed proactively

**📋 Common Use Cases:**
- Monitor **Azure** platform health
- Plan for scheduled maintenance
- Respond quickly to service disruptions
- Historical health tracking

> **💡 EXAM TIP:** Service Health has 3 parts: **Azure** Status (global), Service Health (your services), Resource Health (your resources).

### **Azure** Monitor

**What It Is**: Comprehensive monitoring solution for collecting, analyzing, and acting on telemetry from **Azure** and on-premises.

**What It Monitors**:
- Applications
- Virtual machines
- Containers
- Databases
- Networks
- Guest OS and infrastructure

**Data Types**:
- **Metrics**: Numerical time-series data (CPU%, memory usage, request count)
- **Logs**: Text records of events (application logs, security logs)

**Key Components**:

**Metrics**:
- Real-time numerical data
- 1-minute granularity
- Stored for 93 days
- Lightweight and fast
- Good for alerts and dashboards

**Logs** (via Log Analytics):
- Detailed text-based data
- Query with Kusto Query Language (KQL)
- Retained based on workspace settings
- Good for deep analysis and troubleshooting

**Alerts**:
- React to important conditions
- Metric alerts: When metric crosses threshold
- Log alerts: Based on log query results
- Activity log alerts: **Azure** resource changes
- Action groups: Email, SMS, webhook, automation

**Application Insights**:
- Application Performance Management (APM)
- Monitor live web applications
- Automatically detect performance anomalies
- Track requests, exceptions, dependencies
- Built-in analytics
- Works with .NET, Java, Node.js, Python

**Features**:
- Dashboards and workbooks
- Autoscale based on metrics
- Integration with ITSM tools
- Export data to external systems

> **💡 EXAM TIP:** **Azure** Monitor = comprehensive monitoring platform. Application Insights = specifically for application performance monitoring.

### Log Analytics

**What It Is**: Tool within **Azure** Monitor for querying and analyzing log data.

**Features**:
- Centralized log storage (Log Analytics workspace)
- Query logs with KQL (Kusto Query Language)
- Combine data from multiple sources
- Create visualizations and dashboards
- Set up log-based alerts

**Common Use Cases**:
- Security analysis and threat detection
- Performance troubleshooting
- Usage pattern analysis
- Compliance auditing

**Example Queries**:
```kusto
// Failed login attempts
SecurityEvent
| where EventID == 4625
| summarize count() by Account

// **VM** performance
Perf
| where CounterName == "% Processor Time"
| summarize avg(CounterValue) by Computer
```

> **💡 EXAM TIP:** Log Analytics = query and analyze logs in **Azure** Monitor using KQL.

### Monitoring Comparison

| Service | Purpose | What It Monitors |
|---------|---------|------------------|
| **Advisor** | Best practice recommendations | Configuration and usage patterns |
| **Service Health** | **Azure** platform health | **Azure** service incidents and maintenance |
| ****Azure** Monitor** | Comprehensive monitoring | Metrics and logs from all resources |
| **Application Insights** | Application performance | Web application performance and usage |

> **💡 EXAM TIP:** Know what each monitoring service does and when to use it.


---

## Service Level Agreements (SLAs)

### What is an **SLA**?

> **📖 Definition:** Microsoft's commitment to provide a specific level of service availability and performance.

**Key Concepts**:
- **Uptime guarantee**: Percentage of time service is available
- **Service credits**: Refunds if **SLA** not met
- **Monthly calculation**: **SLA** measured over calendar month
- **Free services have no SLA**: Only paid services have SLAs

### Understanding **SLA** Percentages

**Common **SLA** Levels**:

| **SLA** % | Downtime per Month | Downtime per Year |
|-------|-------------------|-------------------|
| 99% | 7.2 hours | 3.65 days |
| 99.9% | 43.2 minutes | 8.76 hours |
| 99.95% | 21.6 minutes | 4.38 hours |
| 99.99% | 4.32 minutes | 52.56 minutes |
| 99.999% | 26 seconds | 5.26 minutes |

> **💡 EXAM TIP:** Know common **SLA** percentages and approximate downtime. 99.9% ≈ 8.7 hours/year.

### Service-Specific SLAs

**Examples**:
- **Single VM**: 99.9% (with Premium SSD)
- ****VMs** in Availability Set**: 99.95%
- ****VMs** across Availability Zones**: 99.99%
- ****Azure** SQL Database**: 99.99%
- ****Azure** Cosmos DB**: 99.999% (multi-**region**)
- ****Azure** Active Directory**: 99.99%
- ****Azure** Storage**: 99.9% (RA-GRS read), 99.99% (write)

**Factors Affecting SLA**:
- Service tier (Basic vs Premium)
- Configuration (single instance vs redundant)
- Region (single vs multi-**region**)

### Composite **SLA**

**Concept**: When using multiple services, overall **SLA** is product of individual SLAs.

**Example**:
- Web App: 99.95% **SLA**
- **SQL Database**: 99.99% **SLA**
- **Composite SLA**: 99.95% × 99.99% = **99.94%**

**Formula**: SLA₁ × SLA₂ × SLA₃ ... = Composite **SLA**

**Key Point**: Adding services DECREASES overall **SLA** (more potential failure points).

**Improving Composite SLA**:
- Add redundancy (multiple regions)
- Implement fallback mechanisms
- Design for degraded functionality
- Use higher-tier services with better SLAs

> **💡 EXAM TIP:** Composite **SLA** is multiplication of individual SLAs. More dependencies = lower overall **SLA**.

### Designing for **SLA**

**Strategies**:
1. **Avoid single points of failure**: Use availability sets/zones
2. **Replicate across regions**: For disaster recovery
3. **Degrade gracefully**: Provide limited functionality during outages
4. **Use queue-based load leveling**: Buffer between components
5. **Design for self-healing**: Automatic recovery from failures

**Application SLA**:
- Define your own **SLA** targets
- Design architecture to meet targets
- Account for dependencies
- Plan for degraded operations


---

## **Azure** Support Plans

### Support Plan Tiers

**Basic** (Included with all accounts):
- **Cost**: Free
- **Support**: Billing and **subscription** support only
- **Technical support**: None (community forums only)
- **Response time**: N/A
- ****Azure** Advisor**: Yes
- **Service Health**: Yes

**Developer**:
- **Cost**: $29/month
- **Support**: Business hours via email
- **Response time**: <8 hours for minimal business impact
- ****Azure** Advisor**: Yes
- **Best for**: Trial and non-production environments

**Standard**:
- **Cost**: $100/month
- **Support**: 24/7 via email and phone
- **Response time**:
  - Critical: <1 hour
  - Moderate: <4 hours
  - Minimal: <8 hours
- **Architecture guidance**: General
- **Best for**: Production workloads

**Professional Direct**:
- **Cost**: $1,000/month
- **Support**: 24/7 via email and phone
- **Response time**:
  - Critical: <1 hour (with priority)
  - Moderate: <2 hours
  - Minimal: <4 hours
- **Architecture guidance**: Provided by ProDirect delivery manager
- **Operations support**: Webinars, on-demand training
- **Best for**: Business-critical dependence on **Azure**

**Premier** (now Microsoft Unified):
- **Cost**: Custom (contact Microsoft)
- **Support**: 24/7 via email and phone
- **Response time**: <1 hour (critical) with highest priority
- **Technical Account Manager**: Yes
- **Custom support**: Tailored to organization
- **Best for**: Large enterprises with substantial **Azure** usage

### Comparison Table

| Feature | Basic | Developer | Standard | Professional Direct | Premier |
|---------|-------|-----------|----------|---------------------|---------|
| **Cost/month** | Free | $29 | $100 | $1,000 | Custom |
| **Technical Support** | No | Email | 24/7 Email/Phone | 24/7 Email/Phone | 24/7 Email/Phone |
| **Critical Response** | N/A | N/A | <1 hour | <1 hour (priority) | <15 min |
| **Architecture Support** | No | General | General | ProDirect manager | Custom |
| **TAM** | No | No | No | No | Yes |

> **💡 EXAM TIP:** Know the 5 support tiers and what each includes. Remember response times for critical issues.

### Support Scope

**What's Covered**:
- **Azure** platform issues
- Service availability
- Configuration help
- How-to questions
- Billing support (all tiers)

**What's NOT Covered**:
- Code development
- Third-party software support
- On-premises infrastructure (unless using **Azure** Arc)
- General IT consulting

### Support Channels

**Community Support** (Free):
- Microsoft Q&A
- Stack Overflow (azure tag)
- **Azure** documentation
- Community forums

**Knowledge Center**:
- Self-service articles
- Troubleshooting guides
- Best practices

**Support Tickets**:
- Create from **Azure** Portal
- Track progress online
- Escalate as needed

> **💡 EXAM TIP:** All support plans include billing support. Only Developer tier and above get technical support.


---

## Chapter Summary

### Key Concepts to Memorize

**Cost Management**:
- **Factors**: Resource type, consumption, **region**, network traffic
- **Pricing Calculator**: Estimate costs BEFORE deployment
- **TCO Calculator**: Compare on-premises vs **Azure**
- **Cost Management**: Monitor and optimize ACTUAL costs
- **Tags**: Organize and track costs
- **Optimization**: Reserved instances, Hybrid Benefit, right-sizing, spot **VMs**

**Governance**:
- **Microsoft Purview**: Data governance and compliance
- ****Azure** Policy**: Enforce rules and compliance (WHAT)
- **RBAC**: Control access (WHO)
- **Blueprints**: Package templates + policies + **RBAC**
- **Resource Locks**: Prevent deletion (CanNotDelete) or changes (ReadOnly)

**Management Tools**:
- **Portal**: Web-based GUI
- **Cloud Shell**: Browser-based CLI (Bash/PowerShell)
- ****Azure** CLI**: Cross-platform, `az` commands
- **PowerShell**: Cmdlets, `Verb-AzNoun` format
- **ARM**: Deployment layer for all tools
- **ARM Templates**: Infrastructure as Code (JSON)
- ****Azure** Arc**: Manage on-premises/multi-cloud from **Azure**

**Monitoring**:
- **Advisor**: Recommendations (Reliability, Security, Performance, Cost, Ops Excellence)
- **Service Health**: **Azure** platform health (Status, Service Health, Resource Health)
- ****Azure** Monitor**: Metrics and logs monitoring
- **Application Insights**: Application performance monitoring
- **Log Analytics**: Query logs with KQL

**SLAs**:
- 99.9% = ~8.7 hours downtime/year
- 99.99% = ~52 minutes downtime/year
- Composite **SLA** = multiply individual SLAs
- Higher redundancy = better **SLA**

**Support Plans**:
- **Basic**: Free, billing only
- **Developer**: $29, email support
- **Standard**: $100, 24/7 phone
- **Professional Direct**: $1,000, ProDirect manager
- **Premier**: Custom, TAM


---

## Practice Questions

### Question 1
You need to estimate the cost of deploying 50 **VMs** to **Azure** before actually deploying them. Which tool should you use?

A: **Azure** Cost Management

B: **Azure** Pricing Calculator

C: TCO Calculator

D: **Azure** Advisor


---

✅ **Answer:** B

💡 **Explanation:** Pricing Calculator estimates costs BEFORE deployment. Cost Management tracks actual spending after deployment.

---


---

### Question 2
Which tool should you use to compare the costs of running infrastructure on-premises versus in **Azure**?

A: Pricing Calculator

B: Cost Management

C: TCO Calculator

D: **Azure** Advisor


---

✅ **Answer:** C

💡 **Explanation:** TCO (Total Cost of Ownership) Calculator compares on-premises costs vs **Azure** costs to justify migration.

---


---

### Question 3
You need to prevent any user from accidentally deleting a production database. What should you implement?

A: **Azure** Policy

B: **RBAC**

C: Resource lock

D: **Azure** Blueprint


---

✅ **Answer:** C

💡 **Explanation:** Resource locks (CanNotDelete) prevent deletion even for users with permissions. Locks override **RBAC**.

---


---

### Question 4
Which **Azure** tool provides personalized recommendations for cost optimization, security, and performance?

A: **Azure** Monitor

B: **Azure** Advisor

C: Service Health

D: Application Insights


---

✅ **Answer:** B

💡 **Explanation:** Advisor provides free personalized recommendations across 5 categories: Reliability, Security, Performance, Cost, Operational Excellence.

---


---

### Question 5
Your company wants to ensure all virtual machines deployed in **Azure** must be in the West US **region**. What should you use?

A: **RBAC**

B: Resource lock

C: **Azure** Policy

D: Management group


---

✅ **Answer:** C

💡 **Explanation:** **Azure** Policy enforces rules about resource configurations, including allowed locations. **RBAC** controls who can do what, not where.

---


---

### Question 6
What is the composite **SLA** if you use **Azure** App Service (99.95% **SLA**) with **Azure** **SQL Database** (99.99% **SLA**)?

A: 99.99%

B: 99.95%

C: 99.94%

D: 100%


---

✅ **Answer:** C

💡 **Explanation:** Composite **SLA** = 99.95% × 99.99% = 99.94%. Multiply individual SLAs to get composite.

---


---

### Question 7
Which command-line tool uses commands in the format `az <group> <command>`?

A: **Azure** PowerShell

B: **Azure** CLI

C: **Azure** Cloud Shell

D: ARM


---

✅ **Answer:** B

💡 **Explanation:** **Azure** CLI uses `az` commands. PowerShell uses `Verb-AzNoun` format. Cloud Shell is the environment, not a command format.

---


---

### Question 8
You need to manage on-premises servers using **Azure** tools and policies. What should you use?

A: **Azure** Portal

B: **Azure** Arc

C: **Azure** Policy

D: ARM Templates


---

✅ **Answer:** B

💡 **Explanation:** **Azure** Arc extends **Azure** management to on-premises and multi-cloud resources.

---


---

### Question 9
Which **Azure** service provides a personalized view of health issues affecting YOUR **Azure** resources?

A: **Azure** Status

B: Service Health

C: **Azure** Monitor

D: **Azure** Advisor


---

✅ **Answer:** B

💡 **Explanation:** Service Health shows issues affecting services you use. **Azure** Status shows global health. **Azure** Monitor tracks metrics/logs.

---


---

### Question 10
What is the minimum support plan that includes 24/7 technical support via phone?

A: Basic

B: Developer

C: Standard

D: Professional Direct


---

✅ **Answer:** C

💡 **Explanation:** Standard ($100/month) is the first tier with 24/7 phone support. Developer only has business hours email support.

---


---

### Question 11
You want to track **Azure** spending by department for chargeback. What should you use?

A: Resource locks

B: Resource groups

C: Tags

D: **Azure** Policy


---

✅ **Answer:** C

💡 **Explanation:** Tags allow you to organize and track costs by department, project, or any category for chargeback/showback.

---


---

### Question 12
Which type of resource lock prevents both modification and deletion?

A: CanNotDelete

B: ReadOnly

C: DoNotModify

D: Protected


---

✅ **Answer:** B

💡 **Explanation:** ReadOnly prevents all modifications and deletions. CanNotDelete allows modifications but prevents deletion.

---


---

### Question 13
What is the primary purpose of ARM templates?

A: Monitor **Azure** resources

B: Control access to resources

C: Define infrastructure as code

D: Estimate costs


---

✅ **Answer:** C

💡 **Explanation:** ARM templates define **Azure** resources in JSON format for repeatable, consistent deployments (Infrastructure as Code).

---


---

### Question 14
Which **Azure** Monitor component is specifically designed for monitoring web application performance?

A: Metrics

B: Logs

C: Application Insights

D: Service Health


---

✅ **Answer:** C

💡 **Explanation:** Application Insights is the APM (Application Performance Management) component of **Azure** Monitor specifically for web apps.

---


---

### Question 15
An **SLA** of 99.99% allows approximately how much downtime per year?

A: 8.7 hours

B: 52 minutes

C: 4.4 hours

D: 5 minutes


---

✅ **Answer:** B

💡 **Explanation:** 99.99% = 0.01% downtime = approximately 52.56 minutes per year.

---

---


---

## 🎓 Next Steps

Excellent work completing Chapter 3! You now understand **Azure**'s cost management, governance, and monitoring tools.

**Next**: Continue to [Chapter 4: Practice Questions and Exam Scenarios](04-practice-questions.md) to test your knowledge across all domains.

**Review Checklist**:
- Understand difference between Pricing Calculator and TCO Calculator
- Know all cost optimization strategies
- Memorize what **Azure** Policy, **RBAC**, and locks do differently
- Understand all management tools (Portal, CLI, PowerShell, ARM)
- Know monitoring tools and when to use each
- Memorize **SLA** percentages and downtime equivalents
- Know support plan tiers and what each includes
