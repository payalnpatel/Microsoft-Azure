# AZ-900 Study Guide 
Study Guide / Notes created using: https://docs.microsoft.com/en-us/users/23110622/collections/0kjyh8rn5x76j6 

## Describe Cloud Concepts

### Describe Cloud Computing
- <b>Cloud Computing:</b> The delivery of computing services over the internet (which is otherwise known as the cloud).  These services include servers, storage, databases, networking, software, analytics, and intelligence.  Cloud computing offers faster innovation, flexible resources, and economies of scale.  
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
• describe Azure datacenters



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
- <b>Authentication vs. Authorization</b>
  - <b>Authentication (AuthN):</b> the process of establishing the identity of a person or service that wants access to a resource. Involves the act of challenging a part of legitimate credentials and provides the basis for creating a security principal for identity access control.
    - It establishes whether the user is who they say they are. 
    - authentication establishes the user's identity 
  - <b>Authorization (AuthZ):</b> the process of establishing what level of access an authenticated person or service has. 
    - specifies what data they're allowed access to and what they can do with it. 
    - It establishes the level of access that an authenticated user has. 


- <b>Azure Active Directory (Azure AD)</b>: a cloud-based identity and access management service.  Azure AD enables an organization to control access to applications and resources based on its business requirements.  
  - Azure AD provides services such as
    - <b>Authentication</b> - includes verifying identity to access applications and reousrces.  Also includes providing functionaliy such as self-service password reset, MFA, a custom list of banned passwords, and smart lockout services. 
    - <b>Single Sign-On (SSO)</b> - SSO enables you to remember only one username and one password to access multiple applications.  A single identity is tied to a user, which simplifies the security model.  As users change roles or leave an organization, access modifications are tied to that identity, which greatly reduces the effort needed to change or disable accounts. 
    - <b>Application Management</b>
    - <b>Device Management</b> 
  - <b>Azure AD Connect</b> - synchronizes user identities between on-premises Active Directory and Azure AD. 
- Azure Active Directory Domain Services (Azure AD DS) 

- <b>Single Sign-On (SSO):</b> SSO enables a user to sign in one time and use that credential to access multiple resources and applications from different providers. 
- <b>Multifactor Authentication (MFA):</b> MFA is a process where a user is prompted during the sign-in process for an additional form of identification.  Examples include a code from their mobile phone or a fingerprint scan. 
  - MFA provides additional security for your identities by requiring two or more elements to fully authenicate. These elements fall into 3 categories:
    - <b>Something the user <i>knows</i></b> - might be an email address or password
    - <b>Something the user <i>has</i></b> - might be a code that's sent to the user's mobile phone
    - <b>Something the user <i>is</i></b> - typically some sort of biometric property such as a fingerprint or face scan 
  - MFA increase identity security by limiting the impact of credential exposure. 
- Passwordless 
-
descibe external identities and guest access in Azure

- <b>Conditional Access:</b> a tool that Azure AD uses to allow (or deny) access to resources based on identity signals, such as a user's location.
  - These signals include who the user is, where the user is, and what device the user is requesting access from. 
  - Provides a more granular MFA experience for users - i.e. user might not be challenged for a second authentication factor if they are a known location. 
  - During sign-in, Conditional Access collects signals from the user, makes decisions based on those signals, and then enforces that decision by allowing or denying the access request or challenging for a MFA response. 
• describe Azure role-based access control (RBAC)
- <b>Azure Role-Based Access Control (RBAC):</b> enables you to create roles that define access permissions
  - Azure provides built-in roles that define common rules for cloud resources.  You can also define your own roles.  Each role has an associated set of access permissions that relate to that role.  When you assign individuals or groups to one or more roles, they receive all associated access permissions. 
  - RBAC is applied to a scope (which is a resource or set of resources that this access applies to)
  - <b>Role</b> - reader, resource-specific, custom, contributor, owner
  - <b>Scope</b> - management group (a collection of subscriptions), subscription, resource group, resource 
  - RBAC uses an allow model - RBAC  allows you to perform certain actions when you're assigned a role 
  - You can apply Azure RBAC to an individual person or group.  Can also apply to other special identity types, such as service principals and managed identities. 
  - You can manage access permissions on the Access control (IAM) pane in the Azure portal. 
 
- <b>Zero Trust</b> 

- A <b>Defense-in-Depth</b> strategy uses a series of mechanisms to slow the advance of an attack that aims at acquiring unauthorized access to data.  The objective is to protect information and prevent it from being stolen by those who aren't authorized to access it.  
  - Each layer provides protection so that if one layer is breached, a subsequent layer is already in place to prevent further exposure.  This approach removes reliance on any single layer of protection.  It slows down an attack and provides alert telemetry that security teams can act upon, either automatically or manually.  
    - <b>Physical Security</b> - the first line of defense to protect computing hardware in the datacenter 
      - Physically securing access to buildings and controlling access to computing hardware within the datacenter 
    - <b>Identity and Access</b> - controls access to infrastructure and change control 
      - control access to infrastructure and change control
      - use SSO and MFA
      - audit events and changes 
    - <b>Perimeter</b> - uses distributed denial of service (DDoS) protection to filter larger-scale attacks before they can cause a denial of service for users 
      - use DDoS protection to filter large-scale attacks before they can affect the availability of a system for users
      - use perimeter firewalls to identify and alert malicious attacks against your network 
      - at the network perimeter it's about protecting network-based attacks against your resources 
    - <b>Network</b> - limits communications between resources through segmentation and access controls 
      - limit communication between resources
      - deny by default
      - restrict inbound internet access and limit outbound access where appropriate 
      - implement secure connectivity to on-premises networks 
      - at this layer the focus is on limiting network connectivity across all your resource to allow only what's required 
    - <b>Compute</b> - secure access to VMs 
      - implement endpoint protection on devices and keep systems patches and current 
    - <b>Application</b> - helps ensure that apps are secure and free of security vulnerabilities 
      - store sensitive app secrets in a secure storage medium
      - make security a design requirement for all application development
    - <b>Data</b> - controls access to business and customer data that you need to protect
• Describe the purpose of Microsoft Defender for Cloud
## Describe Azure Management and Governance

### Describe Cost Management in Azure
- Factors that affect cost
  -<b> Resource Type</b> - a number of factors influence the cost of Azure resources. They depend on the type of resource or how you customize it. 
    - i.e. type (blob/table storage), performance tier (standard vs. premium), access tier (hot, cool, archive), etc. 
  - <b>Usage Meters:</b> When you provision a resource, Azure creates meters to track that resource's usage. These meters are used to generate a usage record that's later used to help calculate your bill. Each meter tracks a specific type of usage. 
  - <b>Resource Usage:</b> charged based on what you use.
    - Deallocating a VM means VM is no longer running, but the associated hard disks and data are still kept in Azure. (billed for disk storage, but removes compute cost and VM's IP address cost during this time) -- This is a way to minimize costs. 
  - <b>Azure Subscription Types:</b> some Azure subscription types also include usage allowances, which affect costs. 
  - <b>Azure Marketplace:</b> can also purchase Azure-based solutions and services from third-party vendors through Azure Marketplace. 
  - <b>Location:</b> when you provision a resource in Azure, you need to define the location (i.e. Azure region) of where it will be deployed. Different regions can have different associated prices. Geographic regions can affect where your network traffic flows, thus network traffic is a cost influence to consider as well. 
  - <b>Zones for Billing Network Traffic:</b> billing zones are a factor in determining the cost of some Azure services. 
    - <b>Bandwidth</b>  - refers to data moving in and out of Azure datacenters. Some inbound data transfers (data going into Azure datacenters) are free.  For outbound data transfers, data transfer pricing is based on zones. 
  - <b>Zone</b> - a zone is a geographical grouping of Azure regions for billing purposes. 
- <b>Pricing Calculator:</b> use to determine which Azure services best fit your budget. helps determine cost / estimate workload cost 

- <b>Total Cost of Ownership (TCO) Calculator:</b> helps estimate the cost savings of operating your solution on Azure over time compared to operating in your on-prem datacenter. 
- <b>Azure Cost Management and Billing Tool:</b> a free service that helps you understand your Azure bill, manage your account and your subscription, monitor and control Azure spending, and optimize resource use.
  - Features include: reporting, data enrichment, budgets, alerting, and recommendations 
  - use to control spending 
 - <b>Resource tags:</b>  a way to organize your resources.  Tags provide extra information, or metadata, about your resources. 
  - Tags also help you manage costs associated with the different groups of Azure products/resources. 

  
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
- <b>Azure Portal:</b> a web-based user interface you can access virtually ever feature of Azure from.
- <b>Azure PowerShell:</b> a shell which developers and DevOps and IT Professionals can executed commands called cmdlets from.  These commands call the Azure REST API to perform every possible management task in Azure.  Cmdlets can be executed independently or combined into a script file and executed together to orchestrate the route setup/teardown/maintenance of single/multiple resources / the deployment of an entire infrastructure from imperative code 
  - likely to prefer PowerShell if you come from a Windows background 
- <b>Azure CLI:</b> command line interface - an executable program with which a developer, DevOps professional, or IT professional can execute commands in Bash 
  - likely to prefer Azure CLI if you come from a Linux background 
- <b>ARM Templates:</b> Azure Resource Manager templates - describe the resources you want to use in a declarative JSON format.  ARM template is verified before any code is executed to ensure that the resources will be created and connected correctly.  The template then orchestrates the creation of those resources in parallel.  
  - Can include both PowerShell and/or Azure CLI Scripts 
  - Helpful for repeatable deployments done in a consistent manner 
- For one-off scenarios, you may prefer more agile tools like PowerShell, Azure CLI scripts, or the Azure Portal.
- <b>Azure Mobile App</b> - provides iOS and Android access to your Azure resources when you're away from your computer.
- describe Azure Cloud Shell, including Azure CLI and Azure PowerShell
• describe the purpose of Azure Arc
• describe Azure Resource Manager and Azure Resource Manager templates (ARM
templates)

### Describe Monitoring Tools in Azure 
- 3 Primary Azure Monitoring Offerings, each of which is aimed at a specific audience and use case and provides a diverse set of tools, services, programmatic APIs, and more. 
  -  <b>Azure Advisor:</b> evaulates your Azure resources and makes recommendations to help improve reliability, security, and performance, achieve operational excellence, and reduce costs.  Designed to help save you time on cloud optimization.  The recommendation service includes suggested actions you can take right away, postpone, or dismiss.  
      - Recommendations are divided into 5 categories: Reliability, Security, Performance, Cost, Operational Excellence 
      - Used to optimize cost 
  - <b>Azure Monitor:</b> a platform for collecting, analyzing, visualizing, and potentially taking action based on the metric and logging data from your entire Azure and on-prem environment.  
    - Use if you want to keep track of performance or issues related to a specific VM, to set upalerts for key events that are related to specific resources, when you want to measure custom events alongside telemetry data.
    - platform used by application insights   
  - <b>Azure Service Health:</b> provides a personalized view of the health of the Azure services, regions, and resources you rely on.  Helps you keep an eye on several event types (i.e. service issues, planned maintenancees, health advisories, etc) 
