# AZ-900 Study Guide 
Study Guide / Notes created using: https://docs.microsoft.com/en-us/users/23110622/collections/0kjyh8rn5x76j6 

## Describe Cloud Concepts

### Describe Cloud Computing
- <b>Cloud Computing:</b> The delivery of computing services over the internet (which is otherwise known as the cloud).These services include servers, storage, databases, networking, software, analytics, and intelligence.  Cloud computing offers faster innovation, flexible resources, and economies of scale.  
- <b>Shared Responsibility Model:</b> 
- Cloud Models (Public, Private, Hybrid)
  - <b>Public Cloud:</b> services are offered over the public internet and available to anyone who wants to purchase them.  Cloud resources, such as servers and storage, are owned and operated by a third-party cloud service provider, and delivered over the internet.
  - <b>Private Cloud:</b> a private cloud consists of computing resources used exclusively by users from one business or organization.  a private cloud can be physically located at your organization's on-site (on-prem) datacenter, or it can be hosted by a third-party service provider.
  - <b>Hybrid Cloud:</b> a hybrid cloud is a computing environment that combines a public cloud and a private cloud by allowing data and applications to be shared between them. 
- Use cases for each cloud model
- Consumption-based Model:
- Cloud Pricing Models: 

### Describe the Benefits of Using Cloud Services
- Benefits of Cloud Computing 
  - <b>High Availability:</b> depending on the SLA that you choose, your cloud-based applications can provide a continuous user experience with no apparent downtime, even when things go wrong.
  - <b>Scalability:</b> applications in the cloud can scale vertically or horizontally.
    - Scale vertically to increase compute capacity by adding RAM or CPUs to a VM
    - Scaling horizontally increase compute capacity by adding instances of resources, such as VMs, to the configuration.
  - <b>Elasticity:</b> you can configure cloud-based applications to take advantage of autoscaling, so your applications always have the resources they need. 
  - <b>Agility:</b> deploy and configure cloud-based resources quickly as you application requirements change. 
  - <b>Geo-distribution:</b> you can deploy apps and data to regional datacenters around the globe, thereby ensuring that your customers always have the best performance in their region. 
  - <b>Disaster Recovery:</b> by taking advantage of cloud-based backup services, data replication, and geo-distribution, you can deploy your applications with the confidence that comes from knowing that your data is safe in the event of a disaster.   
- Benefits 
• describe the benefits of reliability and predictability in the cloud
• describe the benefits of security and governance in the cloud
• describe the benefits of manageability in the cloud

### Describe Cloud Service Types
- <b>Cloud Service Models:</b> define the different levels of shared responsibility that a cloud provider and cloud tenant are responsible for. 
- <b>Infrastructure as a Service (IaaS):</b> the cloud provider keeps hardware up-to-date, but operating system maintenance and network configuration is up to the cloud tenant.
  - aims to give complete control over the hardware that runs your application 
  - the most flexible cloud service, you configure and manage the hardware for your app
- <b>Platform as a Service (PaaS):</b> the cloud provider managers the VMs and networking resources, and the cloud tenant deploys their apps in to the managed hosting environment.
  - focus on app dev, platform management is handled by the cloud provider 
- <b>Software as a Service (SaaS):</b> the cloud provider manages all aspects of the application environment, such as VMs, networking resources, data storage, and applications.  The cloud tenant only needs to provide their data to the app managed by the cloud provider.
  - software that is centrally hosted and managed for you and your customers/users
Describe cloud service types
• identify appropriate use cases for each cloud service (IaaS, PaaS, SaaS)

## Describe Azure Architecture and Services

### Describe the Core Architectural Components of Azure
- <b>regions:</b> different geographical locations around the globe that contain Azure datacenters. A region is a geographical area on the planet that contains at least one, but potentially multiple datacenters that are nearby and networked together with a low-latency network.  
- 
- Organzinging structure for resources in Azure has 4 levels - management groups, subscriptions, resource groups, and resources 
  - <b>resources:</b> instances of services that you create (i.e. VMs, storage, SQL DBs, etc.) 
    - resources are created in regions 
  - <b>resource groups:</b> resources are combined into resource groups, which act as a logical container into which Azure resources like web apps, databases, and storage accounts are deployed and managed.
  - <b>subscriptions:</b> a subscription groups together user accounts and the resources that have been created by those user accounts.  For each subscription, there are limits or quotas on the amount of resources that you can create and use.  Organizations can use subscriptoins to manage costs and the resources that are created by users, teams, or projects.
  - <b>management groups:</b> these groups help you manage access, policy, and compliance for multiple subscriptions. all subscriptions in a management group automatically inherit the conditions applied to the management group.
    - provides a level of scope above subscriptions.  
- <b>Availability Zone:</b> physically separate datacenters within an Azure region.  Each AZ is made up of one or more datacenters equipped with independent power, cooling, and networking.  An AZ is set up to be an isolation boundary -- if one zone goes down, the other continues working.  Not every region has support for AZs. 
- <b>Region Pairs:</b> Each Azure Region is always paired with another region within the same geography (such as US, Europe, or Asia) at least 300 miles away.  This approach allows for the replication of resources (such as VM storage) across a geography that helps reduce the likelihood of interruptions because of events such as natural disasters, civil unrest, power outages, or physical network outages that affect both regions at once. 

• describe Azure regional, regional pairs, and sovereign regions
• describe availability zones
• describe Azure datacenters
• describe the hierarchy of resource groups, subscriptions, and management groups


### Describe Azure Compute and Networking Services

compare compute types, including container instances, virtual machines (VMs), and functions
• describe VM options, including Azure Virtual Machines, Azure Virtual Machine Scale Sets, availability sets, and Azure Virtual Desktop
• describe resources required for virtual machines
• describe application hosting options, including the Web Apps feature of Azure App
Service, containers, and virtual machines
• describe virtual networking, including the purpose of Azure Virtual Networks, Azure
virtual subnets, peering, Azure DNS, Azure VPN Gateway, and Azure ExpressRoute
• define public and private endpoints
### Describe Azure Storage Services 
- Azure Blob Storage, Azure Disk Storage, Azure File 
- <b>Azure Storage Tiers</b> - Azure provides several access tiers, which you can use to balance your storage costs with your access needs. Only hot and cool access tiers can be set at the account level.  Hot, cool, and archive access tiers can be set at the blob level (during upload or after upload) 
  - <b>Hot Access Tier:</b> optimized for storing data that is accessed frequently (i.e. images on your website) 
  - <b>Cool Access Tier:</b> optimized for data that is infrequently accessed and stored for at least 30 days (i.e. invoices for your customers) 
  - <b>Archive Access Tier:</b> appropriate for data that is rarely accessed and stored for at least 180 days with flexible latency requirements (i.e. for long term backups) 
- -

• compare Azure storage services
• describe storage tiers
• describe redundancy options
• describe storage account options and storage types
• identify options for moving files, including AzCopy, Azure Storage Explorer, and Azure
File Sync
• describe migration options, including Azure Migrate and Azure Data Box
### Describe Azure Identity, Access, and Security 


• describe directory services in Azure, including Azure Active Directory (Azure AD) and Azure Active Directory Domain Services (Azure AD DS)
• describe authentication methods in Azure, including single sign-on (SSO), multifactor authentication, and passwordless
• describe external identities and guest access in Azure
• describe Azure AD Conditional Access
• describe Azure role-based access control (RBAC)
• describe the concept of Zero Trust
• describe the purpose of the defense in depth model
- A <b>Defense-in-Depth</b> strategy uses a series of mechanisms to slow the advance of an attack that aims at acquiring unauthorized access to data.  The objective is to protect information and prevent it from being stolen by those who aren't authorized to access it.  
  - Each layer provides protection so that if one layer is breached, a subsequent layer is already in place to prevent further exposure.  This approach removes reliance on any single layer of protection.  It slows down an attack and provides alert telemetry that security teams can act upon, either automatically or manually.  
    - Physical Security 
    - Identity and Access
    - Perimeter 
    - Network
    - Compute 
    - Application
    - Data 
• Describe the purpose of Microsoft Defender for Cloud
## Describe Azure Management and Governance

### Describe Cost Management in Azure
- Factors that affect cost
  - Resource Type
  - Usage Meters
  - Resource Usage 
  - Azure Subscription Types
  - Azure Marketplace 
  - Location
  - Zones for Billing Network Traffic 
- <b>Pricing Calculator:</b> use to determine which Azure services best fit your budget. helps determine cost --
- <b>Total Cost of Ownership (TCO) Calculator:</b> helps estimate the cost savings of operating your solution on Azure over time compared to operating in your on-prem datacenter. 

- describe factors that can affect costs in Azure
• compare the Pricing calculator and the Total Cost of Ownership (TCO) calculator
• describe the Azure Cost Management and Billing tool
• describe the purpose of tags
### Describe Features and Tools in Azure for Governance and Compliance
- <b>Resource Locks:</b> prevent resources from being accidentally deleted or changed.
  - You can apply locks to a subscription, resource group, or an individual resource.
    - <b>CanNotDelete</b> - means authorized people can still read and mofiy a resource, but they can't delete the resource without first removing the lock
    - <b>ReadOnly</b> - means authorized people can read a resource, but they can't delete or change the resource.
- <b>Azure Policy:</b> a service in Azure that enables you to create, assign, and manage policies that control or audit your resources. 
- <b>Azure Blueprints:</b> enables you to define a repeatable set of governance tools and standard Azure resources that your organization requires. 
  - Azure Blueprints orchestrates the deployment of various resource templates and artifacts such as role assignments, policy assignments, Azure Resource Manager templates, and resource groups.  
• describe the purpose of Azure Blueprints
• describe the purpose of Azure Policy
• describe the purpose of the Service Trust Portal


### Describe Features and Tools for Managing and Deploying Azure Resources 


• describe the Azure portal
- describe Azure Cloud Shell, including Azure CLI and Azure PowerShell
• describe the purpose of Azure Arc
• describe Azure Resource Manager and Azure Resource Manager templates (ARM
templates)

### Describe Monitoring Tools in Azure 

• describe Azure Monitor, including Log Analytics, Azure Monitor alerts, and Application
Insights

- 3 Primary Azure Monitoring Offerings, each of which is aimed at a specific audience and use case and provides a diverse set of tools, services, programmatic APIs, and more. 
  -  <b>Azure Advisor:</b> evaulates your Azure resources and makes recommendations to help improve reliability, security, and performanc,e achieve operational excellence, and reduce costs.  Designed to help save you time on cloud optimization.  The recommendation service includes suggested actions you can take right away, postpone, or dismiss.  
      - Recommendations are divided into 5 categories: Reliability, Security, Performance, Cost, Operational Excellence 
      - Used to optimize cost 
  - <b>Azure Monitor:</b> a platform for collecting, analyzing, visualizing, and potentially taking action based on the metric and logging data from your entire Azure and on-prem environment.  
  - <b>Azure Service Health:</b> provides a personalized view of the health of the Azure services, regions, and resources you rely on.  Helps you keep an eye on several event types (i.e. service issues, planned maintenancees, health advisories, etc) 
