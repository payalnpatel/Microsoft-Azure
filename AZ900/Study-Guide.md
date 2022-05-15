# AZ-900 Study Guide 
Study Guide / Notes created using: https://docs.microsoft.com/en-us/users/23110622/collections/0kjyh8rn5x76j6 

## Describe Cloud Concepts

### Describe Cloud Computing
- <b>Cloud Computing:</b> The delivery of computing services over the internet (which is otherwise known as the cloud).  These services include servers, storage, databases, networking, software, analytics, and intelligence.  Cloud computing offers faster innovation, flexible resources, and economies of scale.  
   - A way to rent compute power and storage from someone else's datacenter. When you're done using them, you give them back. You are only billed for what you use.  The cloud provider takes care of maintaining the underlying infrastructure.
    - <b>Compute Power</b> - how much processing your computer can do.  Can add/remove compute as you need 
    - <b>Storage</b> - volume of data you can store on your computer, traditional computer has limited hardware space, with cloud computing you can request more storage as you need it.  
- <b>Shared Responsibility Model:</b> 
- 3 deployment models for Cloud Computing --> Cloud Models (Public, Private, Hybrid)
  - <b>Public Cloud:</b> services are offered over the public internet and available to anyone who wants to purchase them.  Cloud resources, such as servers and storage, are owned and operated by a third-party cloud service provider, and delivered over the internet.
  - <b>Private Cloud:</b> a private cloud consists of computing resources used exclusively by users from one business or organization.  a private cloud can be physically located at your organization's on-site (on-prem) datacenter, or it can be hosted by a third-party service provider.
  - <b>Hybrid Cloud:</b> a hybrid cloud is a computing environment that combines a public cloud and a private cloud by allowing data and applications to be shared between them. 
- Use cases for each cloud model
- Cloud Pricing Models: 
- <b>Capital Expenditures (CapEx):</b> the up-front spending of money on physical infrastructure, and then deducting that up-front expense over time.  Has a value that reduces over time.
- <b>Operational Expenditures (OpEx):</b> spending money on services or products now, and being billed for them now. You can deduct this expense in the same year you spend it.  There is no up-front cost, as you pay for a service or product as you use it
  - <b>Consumption-based model:</b> end users only pay for the resources that they use
    - no upfront costs 
    - no need to purchase and manage costly infrastructure that users might not use to its fullest 
    - the ability to pay for additional resources when they are needed 
    - the ability to stop paying for resources that are no longer needed 

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
![image](https://user-images.githubusercontent.com/35014868/168485305-618db036-6304-4c3f-aaaf-2b11d912fa57.png)
![image](https://user-images.githubusercontent.com/35014868/168485350-ea661192-08b6-4ae2-8d66-df8f76ec92d7.png)

## Describe Azure Architecture and Services

### Describe the Core Architectural Components of Azure
- <b>regions:</b> different geographical locations around the globe that contain Azure datacenters. A region is a geographical area on the planet that contains at least one, but potentially multiple datacenters that are nearby and networked together with a low-latency network.  
  - Special Azure Regions (for compliance or legal reasons) - US DoD Central, US Gov Virginia, US Gov Iowa, China East, China North, etc. 
  - Regions are used to identify the location for your resources
  - Regions are made up of availability zones
- <b>Availability Zone:</b> physically separate datacenters within an Azure region.  Each AZ is made up of one or more datacenters equipped with independent power, cooling, and networking.  An AZ is set up to be an isolation boundary -- if one zone goes down, the other continues working.  Not every region has support for AZs. 
  - AZs are primarily for VMs, managed disks, load balancers, and SQL databases 
  - AZs are created using one or more datacenters.  There's a minimum of 3 zones within a single region.  It's possible that a large disaster could cause an outage big enough to affect even 2 datacenters. 
- <b>Region Pairs:</b> Each Azure Region is always paired with another region within the same geography (such as US, Europe, or Asia) at least 300 miles away.  This approach allows for the replication of resources (such as VM storage) across a geography that helps reduce the likelihood of interruptions because of events such as natural disasters, civil unrest, power outages, or physical network outages that affect both regions at once. 
- Organzinging structure for resources in Azure has 4 levels - management groups, subscriptions, resource groups, and resources 
  - <b>resources:</b> instances of services that you create (i.e. VMs, storage, SQL DBs, etc.) 
    - resources are created in regions 
    - all resources must be in a resource group 
  - <b>resource groups:</b> resources are combined into resource groups, which act as a logical container into which Azure resources like web apps, databases, and storage accounts are deployed and managed.
    - resource groups can't be nested 
    - if you delete a resource group, all resources contained within it are also deleted 
  - <b>subscriptions:</b> a subscription groups together user accounts and the resources that have been created by those user accounts.  For each subscription, there are limits or quotas on the amount of resources that you can create and use.  Organizations can use subscriptions to manage costs and the resources that are created by users, teams, or projects.
    - Using Azure requires a subscription.  A subscription provides you with authenticated and authorized access to Azure products and services.  It allows you to provision resources.
    - An Azure Subscription is a logical unit of Azure services that links to an Azure account, which is an identity in Azure AD or in a directory that Azure AD trusts.  
    - an account can have one or multiple subscriptions that have different billing models and to which you apply different access-management policies.  
    - two types of subscription boundaries -- billing boundary, and access control boundary 
  - <b>management groups:</b> these groups help you manage access, policy, and compliance for multiple subscriptions. all subscriptions in a management group automatically inherit the conditions applied to the management group.
    - subscriptions within a management group automatically inherit the conditions applied to the management groups
    - each management group and subscription can support only one parent 
    - each management group can have many children 
    - provides a level of scope above subscriptions.  
- <b>Sovereign Regions</b>


### Describe Azure Compute and Networking Services
- <b>Azure Compute:</b> on-demand computing service for running cloud-based applications.  It provides computing resources such as disks, processors, memory, networking, and operating systems.  only pay for what you use.  
- <b>Virtual Machines:</b> software emulations of physical computers.  They include a virtual processor, memory, storage, and networking resources.  
  - VMs provide IaaS and can be used in different ways. 
  - VMs are an ideal choice when you need total control over the OS, the ability to run custom software, and to use custom hosting configurations.  
  - VMs can be created and provisioned within minutes when selecting a preconfigured VM image. An <b>image</b> is a template used to create a VM.  These templates include an OS and often other software, like development tools or web hosting environments. 
- <b>Virtual Machine Scale Sets:</b> an Azure compute resource that you can use to deploy and manage a set of identitcal VMs.  With all VMs configured the same, virtual machine scale sets are designed to support true autoscale.  No pre-provisioning of VMs is required. 
  - lets you create and manage a group of identical, load-balanced VMs.  Number of VMs can automatically increase/decrease in response to demand or a defined schedule.  
- <b>Azure Batch - </b>enables large scale parallel and high-performance computing (HPC) batch jobs with the ability to scale to tens, hundreds, or thousands of VMs 
- <b>Container instances</b> and <b>AKS</b> are Azure Compute resources that you can use to deploy and manage containers
  - Containers are lightweight, virtualized application environments.  They're designed to be quickly created, scaled out, and stopped dynamically. You can run multiple instances of a containerized application on a single host machine. 
  - Containers are a virtualization environment.  You can run multiple containers on a single physical or virtual host.  You don't manage the OS for a container. (VMs can only run one OS at a time) 
  - Containers are managed through a container orchestrator, which can start, stop, and scale out application instances as needed. 
  - <b>AKS</b> - the task of automating, managing, and interacting with a large number of containers is known as orchestration.  AKS is a complete orchestration service for containers with distributed architectures and large volumes of containers.  
  - K8s manages placement of pods, if one of these pods crashes K8s can create a new instance of it -- can move workloads between nodes if needed 
- <b>Serverless Computing:</b> the abstraction of servers, infrastructure, and Operating System.  Azure takes care of managing the server infrastructure and the allocation and deallocation of resources based on demand.  Scaling and performance are handled automatically.  No infrastructure management. Scalability.  Only pay for what you use.
  - Azure has 2 implementations of Serverless Computing:
    - <b>Azure Functions</b> - functions can execute code in almost any modern language 
    - <b>Azure Logic Apps</b> - logic apps are designed in a web-based designed and can execute logic triggered by Azure services without writing any code, 
  - <b>Azure Functions:</b> functions are commonly used when you need to perform work in response to an event (often via a REST request), timer, or message, from another Azure service, and when that work can be completed quickly (within seconds or less).  
    - Functions scale automatically based on demand / with functinos Azure runs code when it's triggered and automatically deallocates resources when the function is finished (with VMs you'd incur costs even when the VM is idle) 
    - Functions are idea when you're only concerned about the code running your service and not the underlying platform or infrastructure. 
    - Functions can be stateless or stateful (stateful passes context through the function to track prior activity, stateless is default) 
    - With functions you right code to complete each step 
  - <b>Azure Logic Apps: </b> execute workflows that are designed to automate business scenarios and are built from predefined logic blocks.  
    - every logic app workflow starts with a trigger, which fires when a specific event happens or when newly available data meets specific criteria 
    - with Logic apps, you use a GUI to define the actions and how they relate to one another.
- <b>Azure Virtual Desktop:</b> a desktop and application virtualization service that runs on the cloud
  - enables your users to use a cloud-hosted version of Windows from any location
  - works across devices - Windows, Mac, Linux, iOS, etc.
  - Simplified Management
  - Performance Management
  - Multi-session Windows 10 Deployment 
- <b>Azure Virtual Network:</b> enables Azure resources, such as VMs, web apps, and databases, to communicate with each other, with users on the internet, and with your on-premise client computers.  Can think of Azure network as an extension of your on-prem network with resources that link to other Azure resources.
  - Azure Virtual Networks provide:
    - <b>Isolation and Segmentation</b>
      - Azure Virtual Network allows you to create multiple isolated virtual networks.  When you set up a virtual network, you define a private IP address space by using either public or private IP address ranges.  The public IP range only exists within the virtual network, and isn't internet routable.  You can divide that IP address space into subnets and allocate part of the define address space to each named subnet. 
    - <b>Internet Communications</b>
      - A VM in Azure can connect to the internet by default.  You can enable incoming connections from the internet by assigning a public IP address to the VM or by putting the VM behind a public load balancer.  For VM management you can connect via the Azure CLI, Remote Desktop Protocol, or Secure Shell 
    - <b>Communicate between Azure resources</b>
      - Virtual Networks can connect not only VMs but other Azure resources such as the App Service, AKS, and Azure VM Scale Sets. 
      - <b>Service Endpoints</b> - can use service endpoints to connect to other Azure resource types such as Azure SQL Dbs, and storage accounts.  This approach enables you to link multiple Azure resources to virtual networks to improve security and provide optimal routing between resources. 
    - <b>Communicate with on-prem resources</b>
      - Azure Virtual Networks enable you to link together your on-premises environment within your Azure subscription
        - <b>Point-to-site virtual private networks</b>
        - <b>Site-to-site virtual private networks: </b> links on-prem VPN device or gateway to Azure VPN gateway in a virtual network.  In effect, the devices in Azure can appear as being on the local network.  This connection is encrypted and works over the internet 
        - <b>Azure ExpressRoute:</b> for environments where you need greater bandwidth and even higher levels of security.  Provides a dedicated private connectivity to Azure that doesn't travel over the internet. 
    - <b>Route Network Traffic</b>
      - By default, Azure routes traffic between subnets on any connected virtual networks, on-prem networks, and the internet.  You can also control routing and override those settings as follows.
        - <b>Route tables</b> - a route table allows you to define rules about how traffic should be directed.  You can create custom route tables that control how packets are routed between subnets.  
        - <b> Border gateway protocol (BGP) </b> works with Azure VPN gateways, Azure Route Server, or Express Route to propagate on-prem BGP routes to Azure Virutal Networks. 
    - <b>Filter Network Traffic </b>
      - Azure Virtual Networks enable you to filter traffic between subnets by using the following approaches
        - <b>Network Security Groups (NSGs)</b> - a network security group is an Azure resource that can contain multiple inbound and outbound security rules. You can define these rules to allow or block traffic, based on factors such as source and destination IP address, port, and protocol 
        - <b>Network Virtual Appliances</b> - a network virtual appliance is a specialized VM that can be compared to a hardened network appliance.  A network virtual appliance carries out a particular network function, such as running a firewall or performing wide area network (WAN) optimization 
    - Connect Virtual Networks 
      - You can link virtual networks together by using <b>network peering</b>. Peering enables resources in each virtual network to communicate with each other.  These virtual networks can be in separate regions, which allows you to create a global interconnected network through Azure.
      - <b>User-defined routes (UDR):</b> a significant update to Azure's virtual networks that allows for greater control over network traffic flow.  This method allows network administrators to control the routing tables between subnets within a VNet, as well as betwen VNets.  
- Setting up a Virtual Network
  - A virtual network needs to exist in a resource group 
  - <b>Address space</b> - when you set up a virtual network, you define the internal address space in Classless interdomain routing (CIDR) format.  This address space needs to be unique within your subscription and any other networks that you can connect to.  (can add address spaces after creating a virtual network) 
  - <b>Subnet</b> - within each virtual network address range, you can create one or more subnets that partition the virtual network's address space.  Routing between subnets will then depend on the default traffic routes.  You can also define custom routes.  alternatively, can define one subnet that encompasses all the virtual networks' address ranges. 
  - Service endpoints - 
  - NAT Gateway
  - Bastion Host - you can select to enable or disable Azure Bastion in your virtual network.  <b>Azure bastion service</b> provides a secure and seamless RDP/SSH connectivity to your VMs directly in the Azure Portal over SSL
  - DDoS Protection Standard
  - <b>Firewall</b> - you can enable or disable Azure firewall. A managed cloud-based network security service that protects your Azure Virtual Network resources.
  - <b>Network security group</b> - have security rules that enable you to filter the type of network traffic that can flow in and out of virtual network subnets and network interfaces.  You can create the network security group separately.  then you associate it with each subnet in the virtual network. 
  - <b>Route table</b> - Azure automatically creates a route table for each subnet within an Azure virtual network and adds system default routes to the table.  You can add custom route tables to modify traffic between subnets and virtual networks 
- <b>VPNs</b> use an encrypted tunnel within another network.  They're typically deployed to connect two or more trusted private networks to one another over an untrusted network (typically the public internet).  Traffic is encrypted while traveling over the untrusted network to prevent eavesdropping or other attacks 
- <b>VPN Gateway: </b> a type of virtual network gateway.  Azure VPN gateway instances are deployed in a dedicated subnet of the virutal network and enable the following 
   - connect on-prem datacenters to virtual networks through a <b>site-to-site connection</b>
   - connect individual devices to virtual networks through a <b>point-to-site connection</b>
   - connect virtual networks to other virtual networks through a <b>network-to-network connection</b>
   - all data transfer is encrypted inside a private tunnel as it crosses the internet.  You can deploy only one VPN gateway in each virtual network, but you can use one gateway to connect to multiple locations, which includes other virtual networks or on-premises datacenters. 
   - when you deploy a VPN gateway, you specify the VPN type -- either policy-based or route-based.  The main difference between these two types of VPN gatewways is how traffic to be encrypted is specified.  In Azure, both types of VPN gateways use a pre-shared key as the only method of authentciation.  Both types rely on Internet Key Exchange (IKE) in either version 1 or version 2 and Internet Protocol Security (PSec).  IKE is used to set up security association (an agreement of encryption) between two endpoints.  This association is then passed to the Ipsec suite, which encrypts and decrypts data packets encapsulated in the VPN tunnel.
      - <b>Policy-Based VPNs</b>
         -  Policy-based VPNs specify statically the IP address of packets that should be encrypted through each tunnel. This type of device evaulates every data packet against those sets of IP addresses to choose the tunnel where that packet is going to be sent through 
         -  Support for IKEv1 only 
         -  use of static routing, where combinations of address prefixes from both networks control how traffic is encrypted and decrypted through the VPN tunnel.  the source and destination of the tunneled networks are declared in the policy and don't need to be declared in the routing tables. 
         -  policy-based VPNs must be used in specific scenarios that require them, such as compatibility with legacy on-premises VPN devices 
      - <b>Route-Based VPNs </b>
         - Ipsec tunnels are modeled as a network interface or virtual tunnel interface 
         - IP routing (either static routes or dynamic routing protocols) decides which one of these tunnel interfaces to use when sending each packet.  
         - Route-based VPNs are the preferred connection method for on-premise devices.  They're more resilient to topology changes such as the creation of new subnets. 
         - use a route-based VPN gateway if you need any of the following:
            - connections between virtual networks 
            - point-to-site connections
            - multi-site connections 
            - coexistence with an Azure ExpressRoute gateway 
         - supports IKEv2
         - uses any-to-any (wildcard) traffic selectors
         - can use dynamic routing protocols, where routing/forwarding tables direct traffic to different Ipsec tunnels 
- Required Azure Resources to Deploy VPN Gateways
   - Virtual Network - deploy a virtual network with enough space for the add'l subnet that you'll need for the VPN gateway.  the address space for this virtual network must not overlap with the on-prem network that you'll be connecting to.  you can deploy only one VPN gateway within a virtual network. 
   - GatewaySubnet - deploy a subnet called GatewaySubnet for the VPN gateway. 
   - Public IP address - create a basic SKU dynamic public IP address if you're using a non-zone-aware gateway.  This address provides a public-routeable IP address as the target for your on-premises VPN device.  This IP address is dynamic but won't change unless you delete or re-create the VPN gateway. 
   - local network gateway - create a local network gateway to define the on-prem network's configuration, such as where the VPN gateway will connect and what it will connect to.  this configuration includes the on-premises VPN device's IPv4 address and the on-prem routable networks. 
   - virtual network gateway - create this to route traffic between the virtual network and the on-prem datacenter or other virtual networks.  the virtual network gateway can be either a VPN or ExpressRoute. 
   - connection - create a connection to create a logical connection between the VPN gateway and the local network gateway. 
      - the connection is made to the on-prem VPN devices IPv4 address as defined by the local network gateway
      - the connection is made from the virtual network gateway and its associated public IP address
      - you can create multiple connections 
- Required On-Prem Resources to Deploy VPN Gateways
   - A VPN device that supports policy-based or route-based VPN gateways
   - a public-facing (internet-routable) IPv4 address 
- <b>Azure ExpressRoute:</b> lets you extend your on-premises network into the Microsoft Cloud over a private connection with the help of a connectivity provider. 
   - ExpressRoute does provide private connectivity, but it isn't encrypted. 
- <b>Public Endpoint:</b> public endpoint for a managed instance enables data access to your managed instance from outside the virtual network.
- <b>Private Endpoint</b> a network interface that uses a private IP address from your virtual network. This network interface connects you privately and securely to a service that's powered by Azure Private Link. By enabling a private endpoint, you're bringing the service into your virtual network


### Describe Azure Storage Services 
- Azure provides 4 main types of storage services
  - <b>Azure Blob storage:</b> storage service for very large object, such as video files or bitmaps
   - Object storage solution for the cloud. Azure Blob Storage is unstructured, meaning that there are no restrictions on the kinds of data it can hold.  Blob storage can manage thousands of simultaneous upoads, massive amounts of video data, constantly growing log files, and can be reached from anywhere with an internet connection. 
   - Blobs aren't limited to file formats 
   - Blob storage is ideal for: serving images or documents directly to a browser, storing files for distributed access, streaming video or audio, storing data for backup and restore/disaster recovery/archiving, storing data for analysis by an on-prem or azure-hosted service, storing up to 8 TB of data for VMs 
   - Can store blob in containers, which helps you organize your blobs depending on your business needs. 
  - <b>Azure File storage:</b> file shares that can be accessed and managed like a file server
   - Offers fully managed file shares in the cloud that are accessible via the industry standard server message block and network file system protocol. 
   - Azure file shares can be mounted concurrently by cloud or on-prem deployments of Windows, Linux, and macOS. 
   - Use Azure File shares for the following - many on-prem apps use file shares (Azure files makes it easier to migrate those apps that share data to Azure), store configuration files on a file share and access them from multiple VMs, write data to a file share and process/analyze the data later. might want to do this with diagnostic logs, metrics, and crash dumps. 
   - Azure files ensures the data is encrypted at rest, and the SMB protocol ensures the data is encrypted in transit. 
   - Can access Azure files from anywhere in the world with a URL that points to the file.  can also use a shared access signature (SAS) token to allow access to a private asset for a specific period of time.  
  - <b>Azure Queue storage:</b> a data store for queing and reliably delivering messages between applications.
  - <b>Azure Table storage</b> - table storage is a service that stores non-relational structured data (also known as structured NoSQL data) in the cloud, providing a key/attribute store with a schemaless design. 
  - These services share several common characteristics:
    - durable and HA with redundancy and replication
    - secure through automatic encryption and role-based access control 
    - scalable with virtually unlimited storage 
    - managed, handling maintenance and any critical problems for you
    - accessible from anywhere in the world over HTTP or HTTPS
- To use Azure storage, you need to create an Azure storage account to store your data objects. 
- Azure VMs use Azure Disk Storage to store virtual disks; however, you can't use Azure Disk Storage to sstore a disk outside of a VM. 
   - <b>Disk storage</b> provides disks for Azure VMs
   - Disks come in many different sizes and performance levels -- from SSDs, to tradditional HDDs with varying performance tiers.  You can use Standard SSD and HDD disks for less critical workloads, premium SSD disks for mission-criticial production apps, and ultra disks for data-intensive workloads such as SAP Hana, top tier databases, and transaction-heavy workloads. 
- <b>Azure Storage Tiers</b> - Azure provides several access tiers, which you can use to balance your storage costs with your access needs. Only hot and cool access tiers can be set at the account level.  Hot, cool, and archive access tiers can be set at the blob level (during upload or after upload) 
  - <b>Hot Access Tier:</b> optimized for storing data that is accessed frequently (i.e. images on your website) 
  - <b>Cool Access Tier:</b> optimized for data that is infrequently accessed and stored for at least 30 days (i.e. invoices for your customers) 
  - <b>Archive Access Tier:</b> appropriate for data that is rarely accessed and stored for at least 180 days with flexible latency requirements (i.e. for long term backups) 
- Options for Moving Files
   - <b>AzCopy</b>
   - <b>Azure Storage Explore</b>
   - <b>Azure File Sync</b> 
- Migration Options
   - <b>Azure Migrate</b>
   - <b>Azure Data Box</b> 

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
- <b>Microsoft Defender:</b>

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
   <img width="847" alt="Screen Shot 2022-05-14 at 4 41 58 PM" src="https://user-images.githubusercontent.com/35014868/168447527-25fdffa9-bd8e-47ed-9e6a-1c0c777b9daf.png">
  Image from: https://docs.microsoft.com/en-us/learn/modules/plan-manage-azure-costs/4-purchase-azure-services

- <b>Total Cost of Ownership (TCO) Calculator:</b> helps estimate the cost savings of operating your solution on Azure over time compared to operating in your on-prem datacenter.
  ![image](https://user-images.githubusercontent.com/35014868/168447569-9e5216f5-8928-400f-85cb-2351d60c7dab.png)
  Image from: https://user-images.githubusercontent.com/35014868/168447569-9e5216f5-8928-400f-85cb-2351d60c7dab.png
  
-[<b>Azure Cost Management and Billing Tool:</b>](https://azure.microsoft.com/en-us/services/cost-management/#overview) a free service that helps you understand your Azure bill, manage your account and your subscription, monitor and control Azure spending, and optimize resource use.
  - Features include: reporting, data enrichment, budgets, alerting, and recommendations 
  - use to control spending 
    <img width="572" alt="Screen Shot 2022-05-14 at 4 51 18 PM" src="https://user-images.githubusercontent.com/35014868/168447762-cca1c904-8d32-4c8d-b33c-2ea4603fb077.png">
    
    Image from: https://azure.microsoft.com/en-us/services/cost-management/#overview

 - <b>Resource tags:</b>  a way to organize your resources.  Tags provide extra information, or metadata, about your resources. 
  - Tags also help you manage costs associated with the different groups of Azure products/resources. 
  - a resource tag consists of a name and a value.  you can assign one or more tags to each Azure resource. 

  
### Describe Features and Tools in Azure for Governance and Compliance
- <b>Resource Locks:</b> prevent resources from being accidentally deleted or changed.
  - You can apply locks to a subscription, resource group, or an individual resource.
    - <b>CanNotDelete</b> - means authorized people can still read and mofiy a resource, but they can't delete the resource without first removing the lock
    - <b>ReadOnly</b> - means authorized people can read a resource, but they can't delete or change the resource.
- <b>Azure Policy:</b> a service in Azure that enables you to create, assign, and manage policies that control or audit your resources. these policies enforce different rules across all of your resource configurations so that those configurations stay compliant with corporate standards. 
   - enables you to define both individual policies and groups of related policies (known as initiatives) 
   - evaluates your resources and highlights resources that aren't compliant with the policies that you've created.  can also prevent noncompliant resources from being created.  
- <b>Azure Blueprints:</b> enables you to define a repeatable set of governance tools and standard Azure resources that your organization requires. 
  - Azure Blueprints orchestrates the deployment of various resource templates and artifacts such as role assignments, policy assignments, Azure Resource Manager templates, and resource groups.  
   - enable you to define the set of standard Azure resources that your organization requires. 
   - BluePrints are versioned.  Govern multiple subscriptions using Azure BluePrints 
   - blueprint definition (what should be deployed, blueprint assignment (what was deployed) 
   - each component in the blueprint definition is known as an artifact.  it is possible for artifacts to have no additional paramters (configurations)  
- <b>Trust Center:</b> showcases Microsoft's principles for maintaining data integrity in the cloud and how Microsoft implements and supports security, privacy, compliance, and transparency in all Microsoft cloud products and services.  
- Azure Compliance Documentation 
- Service Trust Portal


### Describe Features and Tools for Managing and Deploying Azure Resources 
- <b>Azure Portal:</b> a web-based, unified console that provides an alternative to command-line tools.  With the Azure Portal, you can manage your Azure subscription by using a graphical user interface.
  - Designed for resiliency and continuous availability.  It maintains a presence in every Azure datacenter.  This configuration makes the portal resilient to individual datacenter failures and avoids network slowdowns by being close to users.  The Azure portal updates continuously and requires no downtime for maintenance activities. 
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
- <b>Azure Resource Manager:</b> the deployment and management service for Azure.  It provides a management layer that enables you to create, update, and delete resources in your Azure account. 
  - manage your infrastructure through delcarative templates rather than scripts.  A <b> resource manager template</b> is a JSON file that defines what you want to deploy to Azure. 
  - deploy, manage, and monitor all the resources for your solution as a group, rather than handling resources individually 
  - redeploy your solution through the development life cycle 
  - define the dependencies between resources so they're deployed in the correct order
  - apply access control to all services b/c RBAC is natively integrated into the management platform
  - apply tags to resources to logically organizes all the resources in your subscription 
  - clarify your organization's billing by viewing costs for a group of resources that share the same tag 
- <b>ARM Templates:</b>describe the resources you want to use in a declarative JSON format. ARM template is verified before any code is executed to ensure that the resources will be created and connected correctly.  the template then orchestrates the creation of those resources in parallel. 
   - can include both PowerShell and/or Azure CLI scripts 
### Describe Monitoring Tools in Azure 
- 3 Primary Azure Monitoring Offerings, each of which is aimed at a specific audience and use case and provides a diverse set of tools, services, programmatic APIs, and more. 
  -  <b>Azure Advisor:</b> evaulates your Azure resources and makes recommendations to help improve reliability, security, and performance, achieve operational excellence, and reduce costs.  Designed to help save you time on cloud optimization.  The recommendation service includes suggested actions you can take right away, postpone, or dismiss.  
      - Recommendations are divided into 5 categories: Reliability, Security, Performance, Cost, Operational Excellence 
      - Used to optimize cost 
      - use when looking for analysis of your deployed resources 
  - <b>Azure Monitor:</b> a platform for collecting, analyzing, visualizing, and potentially taking action based on the metric and logging data from your entire Azure and on-prem environment.  
    - Use if you want to keep track of performance or issues related to a specific VM, to set upalerts for key events that are related to specific resources, when you want to measure custom events alongside telemetry data.
    - platform used by application insights   
  - <b>Azure Service Health:</b> provides a personalized view of the health of the Azure services, regions, and resources you rely on.  Helps you keep an eye on several event types (i.e. service issues, planned maintenancees, health advisories, etc) 
- <b>Azure Security Center:</b> a monitoring service that provides visibility of your security posture across all of your services, both on Azure and on-prem.  The term security posture refers to cybersecurity policies and controls, as well as how well you can predict, prevent, and respond to security threats. 
   - <b>Secure Score:</b> a measure of an organization's security posture. based on security controls, or groups of related security recommendations. your score is based on the percentage of security controls that you satisfy.  
- <b>Azure Sentinel:</b> is Microsoft's cloud based SIEM (security information and event management) system.  It uses intelligent security analytics and threat analysis
   - enables you to : collect cloud data at scale, detect previously undetected threats, investigate threats with AI, respond to incidents rapidly 
- <b>Azure Key Vault:</b> a centralized cloud service for storing an application's secrets in a single, central location.  it provides secure access to sensitive information by providing access control and logging capabilities.  
   - Azure key vault can: manage secrets, manage encryption keys, manage SSL/TLS certificates, store secrets backed by hardware security modules 
   - Benefits of Azure Key Vault: centralized application secrets, securely stored secrets and keys, access monitoring and access control, simplified administration of application secrets, integration with other Azure services 

## Other 
- <b> Azure Dedicated Host:</b> provides dedicated physical servers to host your Azure VMs for Windows and Linux.  A dedicated host is mapped to a physical server in an Azure Datacenter. A host group is a collection of dedicate hosts.  
   - helps address compliance requirements by deploying workloads in an isolated server 
- <b>Azure Firewall:</b> is managed cloud-based network security service that helps protect resources in your Azure virtual networks.  
   - Azure Firewall is a stateful firewall.  A stateful firewall analyzes the complete context of a network connection, not just an individual packet of network traffic.  Azure firewall features HA and unrestricted cloud scalability.  
-<b>Azure Application Gateway:</b> provides a firewall that's called the web application firewall (WAF).  WAF provides centralized, inbound protection for your web applications against common exploits and vulnerabilities.  
- DDoS Protection can help prevent volumetric attacks (goal of attack is to flood network with large amount of semingly legitimate traffic), protocol attacks (exploint weakness in layer 3 and 4 protocol stack), resource layer (app-layer) attacks (only with web app firewall) 
- Azure firewall and Azure DDoS protection can help control what traffic can come from outside sources. 
- A <b>Network Security Group (NSG)</b> enables you to filter network traffic to and from Azure resources within an Azure Virtual Network. you can think of NSGs as an <b>internal firewall. </b> An NSG can contain multiple inbound and outbound security rules that enable you to filter traffic to and from resources by source and destination IP address, port and protocol.  
