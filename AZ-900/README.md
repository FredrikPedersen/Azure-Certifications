# [Azure Fundamentals](https://learn.microsoft.com/en-us/certifications/resources/study-guides/AZ-900)

[1 Cloud Computing](#ins1-cloud-computingins)
 - [1.1 What is cloud computing](#inswhat-is-cloud-computingins)
 - [1.2 The shared responsibility model](#insthe-shared-responsibility-modelins)
 - [1.3 Cloud Models](#inscloud-modelsins)
 - [1.4 The Consumption Based Model](#insthe-consumption-based-modelins)  

[2 The Benefits of Using Cloud Services](#ins2-the-benefits-of-using-cloud-servicesins)
 - [2.1 High Availability](#inshigh-availabilityins)
 - [2.2 Scalability](#insscalabilityins)
 - [2.3 Reliability](#insreliabilityins)
 - [2.4 Security and Governance](#inssecurity-and-governanceins)
 - [2.5 Manageability](#insmanageabilityins)

[3 Cloud Service Types](#ins3-cloud-service-typesins)
 - [3.1 Infrastructure as a Service (Iaas)](#insinfrastructure-as-a-serviceins)
 - [3.2 Platform as a Service (PaaS)](#insplatform-as-a-serviceins)
 - [3.3 Software as a Service (SaaS)](#inssoftware-as-a-serviceins)

[4 Core Architectural Components of Azure](#ins4-core-architectural-components-of-azureins)
 - [4.1 Physical Infrastructure](#ins-physical-infrastructure-ins)
 - [4.2 Management Infrastructure](#ins-management-infrastructure-ins)

[5 Compute and Networking Services](#ins5-compute-and-networking-services-ins)
 - [5.1 Virtual Machines](#ins-virtual-machines-ins)
 - [5.2 Virtual Desktop](#ins-azure-virtual-desktop-ins)
 - [5.3 Containers](#ins-azure-containers-ins)
 - [5.4 Functions](#ins-azure-functions-ins)
 - [5.5 Application Hosting Options](#ins-application-hosting-options-ins)
 - [5.6 Virtual Networking](#ins-virtual-networking-ins)
 - [5.7 Virtual Private Networks](#ins-virtual-private-networks-ins)
 - [5.8 Express Route](#ins-expressroute-ins)

[6 Storage Services](#ins-6-storage-services-ins)
 - [6.1 Storage Accounts](#ins-storage-accounts-ins)
 - [6.2 Storage Redundancy](#ins-storage-redundancy-ins)


## <ins>1 Cloud Computing</ins>

### <ins>What is cloud computing?</ins>

**Cloud computing is the delivery of computing services over the internet**. Computing services include common
IT infrastructure such as virtual machines, storage, databases and networking.  

Because cloud computing uses the internet to deliver these services, it doesn't have to be constrained by 
physical infrastructure the same way that a traditional datacenter is. This mean you can rapidly increase
and decrease your IT infrastructure on-demand.

The base services of any cloud provider is Compute Power and Storage.

### <ins>The shared responsibility model</ins>

The shared responsibility model describes which party is responsible for what parts of the hard- and software.  
In the traditional datacenter, the owning company is responsible for maintaining the physical space, ensuring security
and mainting servers. An IT department will likewise be responsible for maintaining security and software in the 
digital space.

With the shared responsibility model, these responsibilities get shared between the cloud provider and the consumer.
 - Physical security, power, cooling, and network connectivity are the responsibility of the cloud provider
 - The consumer is responsible for the data and information stored in the cloud. The consumer is also responsible for access security, meaning you only give access to those who need it

The shared responsibility model is heavily tied into the cloud service types: 
**Infrastructure as a service (IaaS)**, **Platform as a service (PaaS)**, and **Software as a service (SaaS)**. 
IaaS places the most responsibility on the consumer, with the cloud provider being responsible for the basics of 
physical security, power, and connectivity. On the other end of the spectrum, SaaS places most of the responsibility 
with the cloud provider. PaaS, being a middle ground between IaaS and SaaS, rests somewhere in the middle and evenly 
distributes responsibility between the cloud provider and the consumer.

<img alt="Cloud Service Types" src="https://learn.microsoft.com/en-us/training/wwl-azure/describe-cloud-compute/media/shared-responsibility-b3829bfe.svg" width="1000px"/>

You’ll always be responsible for:
 - The information and data stored in the cloud 
 - Devices that are allowed to connect to your cloud (cell phones, computers, and so on)
 - The accounts and identities of the people, services, and devices within your organization

The cloud provider is always responsible for:
 - The physical datacenter 
 - The physical network 
 - The physical hosts

Your service model will determine responsibility for things like:
 - Operating systems 
 - Network controls 
 - Applications 
 - Identity and infrastructure

### <ins>Cloud Models</ins>

Cloud models define the deployment type of cloud resources.  
The three main cloud models are: private, public and hybrid.

#### <ins>Private Cloud</ins>

A private cloud is the natural evolution from a corporate datacenter. It's a cloud that's used by a single entity.
Private cloud provides much grater control for the company and its IT department. However, it also comes with greater cost and 
fewer of the benefits of a public cloud deployment. Finally, a private cloud may be hosted from your on site datacenter. 
It may also be hosted in a dedicated datacenter offsite, potentially even by a third party that has dedicated that 
datacenter to your company.

#### <ins>Public Cloud</ins>

A public cloud is built, controlled and maintained by a third-party cloud provider. With a public clopud, anyone that wants
to purchase cloud services can access and use resources.

#### <ins>Hybrid Cloud</ins>

A hybrid cloud is a
computing environment that uses both public and private clouds in an inter-connected environment.
A hybrid cloud environment can be used to allow a private cloud to surge for increased, temporary demand by deploying
public cloud resources. Hybrid cloud can be used to provide an extra layer of security. 

| Public Cloud                                                          | Private Cloud                                                      | Hybrid Cloud                                                      |
|-----------------------------------------------------------------------|--------------------------------------------------------------------|-------------------------------------------------------------------|
| No capital expenditures to scale up                                   | Organizations have complete control over resources and security    | Provides the most flexibility                                     |
| Applications can be quickly provisioned and deprovisioned             | Data is not collocated with other organizations’ data              | Organizations determine where to run their applications           |
| Organizations pay only for what they use                              | Hardware must be purchased for startup and maintenance             | Organizations control security, compliance, or legal requirements |
| Organizations don’t have complete control over resources and security | Organizations are responsible for hardware maintenance and updates |                                                                   |

#### <ins>Multi-cloud</ins>

In a multi-cloud scenario, you use multiple public cloud providers. Maybe you use different features from different 
cloud providers. Or maybe you started your cloud journey with one provider and are in the process of migrating to a 
different provider. Regardless, in a multi-cloud environment you deal with two (or more) public cloud providers and 
manage resources and security in both environments.

### <ins>The Consumption Based Model</ins>

When comparing IT infrastructure models, there are two types of expenses to consider. Capital expenditure (CapEx) and
operational expenditure (OpEx).

CapEx is typically a one-time, up-front expenditure to purchase or secure tangible resources. A new building, repaving 
the parking lot and building a datacenter are examples of CapEx.  

OpEx is spending money on services or products over time. Renting a convention center, leasing a company vehicle and
signing up for cloud services are all examples of OpEx.  

Cloud computing falls under OpEx because cloud computing operates on a consumption-based model.
You pay for the IT resources you use, and if you don't use any IT resources this month, you don't pay for it.

The consumption based model has many benefits, including:
 - No upfront costs. 
 - No need to purchase and manage costly infrastructure that users might not use to its fullest potential. 
 - The ability to pay for more resources when they're needed. 
 - The ability to stop paying for resources that are no longer needed.

## <ins>2 The Benefits of Using Cloud Services</ins>

When building or deploying a cloud application, two of the biggest considerations are uptime (or availability) and the 
ability to handle demand (or scale).

### <ins>High Availability</ins>

When you're deploying an application, a service or any IT resources, it's important the resources are available when
needed. Highh availability focuses on ensuring maximum availability, regardless of disruptions or event that may occur.

When you’re architecting your solution, you’ll need to account for service availability guarantees. Azure is a highly 
available cloud environment with uptime guarantees depending on the service. These guarantees are part of the service-level 
agreements (SLAs).

### <ins>Scalability</ins>

Another major benefit of cloud computing is the scalability of cloud resources. Scalability refers to the ability to adjust
resources to meet demand. The ability to scale means you can add or subtract resources to better fit the system demands.

The other benefit of scalability is that you aren't overpaying for services. Because the cloud is a consumption-based model,
you only pay for what you use.

Scaling generally comes in two varieties: vertical and horizontal.   
Vertical scaling is focused on increasing or decreasing the capabilities of resources. Horizontal scaling is adding or 
subtracting the number of resources.

#### <ins>Vertical Scaling</ins>

With vertical scaling, you scale up or down resource components to change processing power, storage capacity etc, as
in if you add more RAM or CPUs to a virtual machine.

#### <ins>Horizontal Scaling</ins>

With horizontal scaling, you manually or automatically add or subtract the amount of available resources, like 
virtual machines and containers. Reducing resources is known as scaling in, while increasing is known as scaling out.

### <ins>Reliability</ins>

Reliability is the ability of a system to recover from failures and continue to function. 
The cloud consists of a decentralized design, and naturally supports a reliable and resilient infrastructure.


### <ins>Predictability</ins>

Predictability can be focused on performance or cost predictability. Utilising the Microsoft Azure Well-Architected Framework,
you can deploy a solution whose cost and performance are predictable.

#### <ins>Performance</ins>

Performance predictability focuses on predicting the resources needed to deliver a positive experience for your customers. 
Autoscaling, load balancing and high availability are just some of the cloud concepts that support performance predictability.

#### <ins>Cost</ins>

Cost predictability is focused on predicting or forecasting the cost of the cloud spend. You can track your resource 
use in real time and monitor resources to ensure that you’re using them in the most efficient way.  

You can even use tools like the Total Cost of Ownership (TCO) or Pricing Calculator to get an estimate of potential cloud spend.

### <ins>Security and Governance</ins>

Cloud features supports governance and compliance. Things like set templates help ensure that all your deployed resources
meet corporate standards and government regulatory requirements. All of your existing resources can of course be updated
as these standards change.

Software patches and updates may also automatically be applied, which helps with both governance and security.

If you want maximum control of security, infrastructure as a service provides you with physical resources but lets you 
manage the operating systems and installed software. If you want patches and maintenance taken care of automatically, 
platform as a service or software as a service deployments may be the best cloud strategies for you.

### <ins>Manageability</ins>

A major benefit of cloud computing is the manageability options. There are two types of manageability:

#### <ins>Management of the Cloud</ins>

Management of the cloud speaks to managing your cloud resources. In the cloud, you can:
 - Automatically scale resource deployment based on need.
 - Deploy resources based on a preconfigured template, removing the need for manual configuration.
 - Monitor the health of resources and automatically replace failing resources.
 - Receive automatic alerts based on configured metrics, so you're aware of performance in real time.

#### <ins>Management in the Cloud</ins>
Management in the cloud speaks to how you're able to manage your cloud environment and resources. You can manage these:
 - Through a web portal
 - Using a command line interface
 - Using APIs
 - Using PowerShell

## <ins>3 Cloud Service Types</ins>

<img alt="Cloud Service Types" src="https://learn.microsoft.com/en-us/training/wwl-azure/describe-cloud-compute/media/shared-responsibility-b3829bfe.svg" width="1000px"/>

### <ins>Infrastructure as a Service</ins>

Infrastructure as a Service is the most flexible category of cloud services. It provides you the maximum amount of control
of your cloud services. In an IaaS model, the cloud provider is responsible for maintaining the hardware, network connectivity, 
and physical security. You’re responsible for everything else: operating system installation, configuration, 
and maintenance; network configuration; database and storage configuration; and so on. 

With IaaS, you’re essentially renting the hardware in a cloud datacenter, but what you do with that hardware is up to you.

#### <ins>Scenarios</ins>
 - Lift-and-shift migration: You're standing up cloud resources similar to your on-prem datacenter, and then simply moving the thing running on-prem to running on the IaaS infrastructure
 - Testing and development: You have established configurations for development and test environments that you need to rapidly replicate. 

### <ins>Platform as a Service</ins>

Platform as a service (PaaS) is a middle ground between renting space in a datacenter (IaaS) and paying for a complete 
and deployed solution (SaaS). In a PaaS environment, the cloud provider maintains the physical infrastructure, 
physical security, and connection to the internet. They also maintain the operating systems, middleware, 
development tools, and business intelligence services that make up a cloud solution. In a PaaS scenario, you don't have 
to worry about the licensing or patching for operating systems and databases.

PaaS is well suited to provide a complete development environment without the headache of maintaining all the 
development infrastructure.

#### <ins>Scenarios</ins>
 - Development framework: PaaS provides a framework that developers can build upon to develop or customize cloud-based applications. Similar to the way you create an Excel macro, PaaS lets developers create applications using built-in software components.
 - Analytics or business intelligence: Tools provided as a service with PaaS allow organizations to analyze and mine their data, finding insights and patterns and predicting outcomes to improve forecasting, product design decisions, investment returns, and other business decisions.

### <ins>Software as a Service</ins>

Software as a service (SaaS) is the most complete cloud service model from a product perspective. With SaaS, you’re 
essentially renting or using a fully developed application. Email, financial software, messaging applications, 
and connectivity software are all common examples of a SaaS implementation.

While the SaaS model may be the least flexible, it’s also the easiest to get up and running. It requires the least 
amount of technical knowledge or expertise to fully employ.

#### <ins>Scenarios</ins>
 - Email and messaging.
 - Business productivity applications.
 - Finance and expense tracking.

## <ins>4 Core Architectural Components of Azure</ins>

The core architectural components of Azure may be broken down into two main groupings: the physical infrastructure, and 
the management infrastructure.

### <ins> Physical Infrastructure </ins>

The physical infrastructure for Azure starts with datacenters. Conceptually, the datacenters are the same as large
corporate datacenters. They're facilities with resources arranged in rack, with dedicated power, cooling and networking 
infrastructure.

Azure has datacenters around the world. They are however, not directly accessible, and are grouped into Azure Regions
or Azure Availability Zones that are designed to help you achieve resiliency and reliability.

#### <ins> Regions </ins>

A region is a geographical area on the planet that contains at least one, but potentially multiple datacenters that are
nearby and networked together with a low-latency network. Azure intelligently assigns and controls the resources within
each region to ensure workloads are appropriately balenced.

When you deploy a resource in Azure, you'll often need to choose the region where you want your resource deployed.

#### <ins> Availability Zones </ins>

Availability Zones are physically separate datacenters within an Azure Region. Each availability zone is made up of one 
or more datacenters equipped with independent power, cooling and networking. An availability zones is set up to be an 
isolation boundry. If one zone goes down, the other continues working.

A minimum of three availability zones are present in all availability zone-enabled regions, but not all Azure Regions currently
support availability zones.

<img alt="Availability Zones diagram" src="https://learn.microsoft.com/en-us/training/wwl-azure/describe-core-architectural-components-of-azure/media/availability-zones-c22f95a3.png"/>

#### <ins> Availability Zones in Apps </ins>

You want to ensure your services and data are redundant so you can protect your information in case of failure.
When you host your infrastructure, setting up your own redundancy requires that you create duplicate hardware environments.

You can use availability zones to run mission-critical applications and build high-availability into your application
architecture by co-locating your resources within an availability zone and replicating in other availability zones.

Availability zones are primarily for VMs, managed disks, load balancers, and SQL databases. Azure services that support 
availability zones fall into three categories:
 - Zonal services: You pin the resource to a specific zone (for example, VMs, managed disks, IP addresses).
 - Zone-redundant services: The platform replicates automatically across zones (for example, zone-redundant storage, SQL Database).
 - Non-regional services: Services are always available from Azure geographies and are resilient to zone-wide outages as well as region-wide outages.

#### <ins> Region Pairs </ins>

Region pairs is like availability zones, but for entire regions instead.

Most Azure regions are paired with another region within the same geography (such as US, Europe or Asia), at least 300
miles away. Because the pair of regions are directly connected and far enough apart to be isolated from regional disasters,
you can use them to provide reliable services and data redundancy.

<img alt="Region Pair diagram" src="https://learn.microsoft.com/en-us/training/wwl-azure/describe-core-architectural-components-of-azure/media/region-pairs-7c495a33.png"/>

#### <ins> Sovereign Regions </ins>

In addition to regular regions, Azure also has sovereign regions. Sovereign regions are instances of Azure that are isolated
from the main instance of Azure. YOu may need to use a sovereign region for compliance or legal purposes.

### <ins> Management Infrastructure </ins>

The management infrastructure includes Azure resources and resource groups, subscriptions and accounts.
Understanding the hierarchical organization will help you plan projects and products within Azure.

#### <ins> Resources and Resource Groups </ins>

A resource is the basic building block of Azure. Anything you create, provision, deploy, etc. is a resource.
Resource Groups are simply groupings of resources. When you create a resource, you're required to place it into a resource group.
While a resource group can contain many resources, a single resource can only be in one resource group, and resource groups can't be nested.

When you apply an action to a resource group, that action will apply to all the resources within the group, e.g if you grant access
to a resource group, you grant access to all the resources within it.

There aren't any hard rules about how you use resource groups, so consider how to set up resource groups to maximize their
usefulnes to you.

#### <ins> Azure Subscriptions </ins>

In Azure, subscriptions are a unit of management, billing, and scale. 
Similar to how resource groups are a way to logically organize resources, subscriptions allow you to logically organize
your resource groups and facilitate billing.

<img alt="subscriptions model" src="https://learn.microsoft.com/en-us/training/wwl-azure/describe-core-architectural-components-of-azure/media/subscriptions-d415577b.png"/>

Using Azure requires an Azure subscription. A subscription provides you with authenticated and authorized access to Azure
products and services. It also allows you to provision resources. An Azure subscription links to an Azure account, 
which is an identity in Azure Active Directory (Azure AD) or in a directory that Azure AD trusts.

An account can have multiple subscriptions, but only one is required.  In a multi-subscription account,
you can use Azure subscriptions to define boundaries around Azure products, services, and resources. 
There are two types of subscription boundaries that you can use:

 - **Billing boundary**: This subscription type determines how an Azure account is billed for using Azure. 
You can create multiple subscriptions for different types of billing requirements. Azure generates 
separate billing reports and invoices for each subscription so that you can organize and manage costs.
 - **Access control boundary**: Azure applies access-management policies at the subscription level, 
and you can create separate subscriptions to reflect different organizational structures. An example 
is that within a business, you have different departments to which you apply distinct Azure subscription policies. 
This billing model allows you to manage and control access to the resources that users provision with specific 
subscriptions.

#### <ins> Azure Management Groups </ins>

At the top of the management infrastructure, we have management groups.
Resources are gathered in resource groups, resource groups are gathered into subscriptions.
If you're dealing with multiple applications, development teams or geographies over multiple subscriptions, you might need
a way to efficiently manage access, policies and compliance for those subscriptions.

Azure management groups provide a level of scope above subscriptions. You organize subscriptions into containers called
management groups and apply governance conditions to the management groups.

Management groups can be nested.

#### <ins> Management group, subscriptions, and resource group hierarchy </ins>

You can build a flexible structure of management groups and subscriptions to organize your resources into a hierarchy 
for unified policy and access management.

<img alt="management group hierarchy diagram" src="https://learn.microsoft.com/en-us/training/wwl-azure/describe-core-architectural-components-of-azure/media/management-groups-subscriptions-dfd5a108.png">

Some examples of how you could use management groups might be:

 - **Create a hierarchy that applies a policy**. You could limit VM locations to the US West Region in a group called Production. 
This policy will inherit onto all the subscriptions that are descendants of that management group and will apply to all 
VMs under those subscriptions. This security policy can't be altered by the resource or subscription owner, which allows 
for improved governance.
 - **Provide user access to multiple subscriptions**. By moving multiple subscriptions under a management group, you can 
create one Azure role-based access control (Azure RBAC) assignment on the management group. Assigning Azure RBAC at the 
management group level means that all sub-management groups, subscriptions, resource groups, and resources underneath 
that management group would also inherit those permissions. One assignment on the management group can enable users to 
have access to everything they need instead of scripting Azure RBAC over different subscriptions.

## <ins>5 Compute and Networking Services </ins>

### <ins> Virtual Machines </ins>

With Azure Virtual Machines, you can create and use VMs in the cloud.
VMs provide IaaS in the form of a virtualized server, and can be used in many ways.
VMs are ideal when you need:
 - Total control over the operating system
 - The ability to run custom software
 - To use custom hosting configurations

You can create or use an already created image to rapidly provision VMS.
A preconfigured image is a template used to create a VM and may already include OS and other software, and let's
you provision av VM in minutes.

#### <ins> Scale VMs in Azure </ins>

You can run single VMs for testing, development or other tasks, or you can group VMs together to provide high
availability, scalability and redundancy.

Virtual machine scale lets you create nd manage a group of identical, load-balanced VMs. If you simply created multiple
VMs with the same purpose, you'd need to ensure they were all configured identically and then set up network
routing parameters to ensure efficiency. You’d also have to monitor the utilization to determine if you need to increase 
or decrease the number of VMs.

Instead, with VM scale sets, Azure automates most of that work. It enables you to centrally manage, configure and update 
a large number of VMs.

#### <ins> Virtual Machine availability sets </ins>

VM availability sets are another tool to help you build a more resilient, highly available environment.
Availability sets are designed to ensure that VMs stagger updates and have varied power and network connectivity,
preventing you from losing all your VMs with a single network or power failure.

Availability sets do this by grouping VMs in two ways: update domain and fault domain.

 - **Update domain:** The update domain groups VMs that can be rebooted at the same time. This allows you to apply updates 
while knowing that only one update domain grouping will be offline at a time. All of the machines in one update domain 
will be updated. 
 - **Fault domain:** The fault domain groups your VMs by common power source and network switch. 
This helps protect against a physical power or networking failure by having VMs connected to different power and 
networking resources.

#### <ins> When to use VMS </ins>

 - During testing and development. VMs provide a quick and easy way to create different OS and application configurations.
Test and development personnel can then easily delete the VMs when they no longer need them.
 - When running applications in the cloud. The ability to run certain applications in the public cloud as opposed to 
creating a traditional infrastructure to run them can provide substantial economic benefits. For example, an application 
might need to handle fluctuations in demand. Shutting down VMs when you don't need them or quickly starting them up to
meet a sudden increase in demand means you pay only for the resources you use.
 - When extending your datacenter to the cloud: An organization can extend the capabilities of its own on-premises 
network by creating a virtual network in Azure and adding VMs to that virtual network. Applications like SharePoint can
then run on an Azure VM instead of running locally. This arrangement makes it easier or less expensive to deploy than in
an on-premises environment.
 - During disaster recovery: As with running certain types of applications in the cloud and extending an on-premises 
network to the cloud, you can get significant cost savings by using an IaaS-based approach to disaster recovery. 
If a primary datacenter fails, you can create VMs running on Azure to run your critical applications and then shut them 
down when the primary datacenter becomes operational again.

### <ins> Azure Virtual Desktop </ins>

Another type of virtual machine is the Azure Virtual Desktop. Azure Virtual Desktop is a desktop and application
virtualization service that runs on the cloud. It enables you to use a cloud-hosted version of Windows from any location. 

Azure Virtual Desktop provides centralized security management for users' desktops with Azure Active Directory (Azure AD).
You can enable multifactor authentication to secure user sign-ins, and secure access to data by assigning 
granular role-based access controls (RBACs) to users.

The data and apps are separated from the local hardware. The actual desktop and apps are running in the cloud.

### <ins> Azure Containers </ins>

If you want to run multiple instances of an application on a single host machine, containers are an excellent choice.
Containers are a virtualization environment. Much like running multiple virtual machines on a single physical host, you 
can run multiple containers on a single physical or virtual host.

Containers are lightweight and designed to be created, scaled out, and stopped dynamically. 
It's possible to create and deploy virtual machines as application demand increases, but containers are a 
lighter weight, more agile method. 

 - **Azure Container Instances:**  Azure Container Instances offer the fastest and simplest way to run a container in 
Azure; without having to manage any virtual machines or adopt any additional services. Azure Container Instances are a PaaS offering. 
 - **Azure Kubernetes Service:** Azure Kubernetes Service (AKS) is a container orchestration service. An orchestration 
service manages the lifecycle of containers. When you're deploying a fleet of containers, AKS can make fleet management simpler and more efficient.

### <ins> Azure Functions </ins>

Azure functions is an event-driven, serverless compute option that doesn't require maintaining VMs or containers.
If you build an app using VMs or containers, those resources have to be "running" in order for you app to function.
With Azure Functions, an event awakens the function, alleviating the need to keep resources provisioned when 
there are no events.

Using Azure Functions is ideal when you're only concerned about the code running your service and not about the underlying
platform or infrastructure.  Functions are commonly used when you need to perform work in response to an event 
(often via a REST request), timer, or message from another Azure service, and when that work can be completed quickly, 
within seconds or less.

Azure Functions runs your code when it's triggered and automatically deallocates resources when the function is finished. 
In this model, you're only charged for the CPU time used while your function runs.

Functions can be either stateless or stateful. When they're stateless (the default), they behave as if they're restarted
every time they respond to an event. When they're stateful (called Durable Functions), a context is passed through the 
function to track prior activity.

### <ins> Application Hosting Options </ins>

If you need to host your applications on Azure, you might initially turn to a VM or containers.
While both VMs and containers provide excellent, robust and dynamic hosting solutions, there are other hosting options 
that you can use with Azure, including Azure App Service.

App Service enables you to build and host web apps, background jobs, mobile back-ends and RESTful APIs in the programming
language of you choice without managing infrastructure.

Types of App Services:
 - Web Apps
   - App Service includes full support for hosting web apps by using ASP.NET, ASP.NET Core, Java, Ruby, Node.js, PHP, or Python. You can choose either Windows or Linux as the host operating system.
 - API Apps
   - Much like hosting a website, you can build REST-based web APIs by using your choice of language and framework. 
   - You get full Swagger support and the ability to package and publish your API in Azure Marketplace. The produced apps can be consumed from any HTTP- or HTTPS-based client.
 - WebJobs
   - You can use the WebJobs feature to run a program (.exe, Java, PHP, Python, or Node.js) or script (.cmd, .bat, PowerShell, or Bash) in the same context as a web app, API app, or mobile app. 
   - They can be scheduled or run by a trigger.
   - WebJobs are often used to run background tasks as part of your application logic.
 - Mobile Apps
   - Use the Mobile Apps feature of App Service to quickly build a back end for iOS and Android apps
   - There's SDK support for native iOS and Android, Xamarin, and React native apps.

App Service handles most of the infrastructure decisions you deal with in hosting web-accessible apps:
 - Deployment and management are integrated into the platform.
 - Endpoints can be secured.
 - Sites can be scaled quickly to handle high traffic loads.
 - The built-in load balancing and traffic manager provide high availability.

### <ins> Virtual Networking </ins>

Azure virtual networks and virtual subnets enable Azure resources to communicate with each other, with users on the internet,
and with your on-premises client computers. You can think of an Azure network as an extension of your on-premises
network with resources that link other Azure resources.

Azure virtual networks provide the following key networking capabilities:
 - Isolation and segmentation
 - Internet communications
 - Communicate between Azure resources 
 - Communicate with on-premises resources 
 - Route network traffic 
 - Filter network traffic 
 - Connect virtual networks

Azure virtual networking supports both public and private endpoints to enable communication between external or internal 
resources with other internal resources.

 - Public endpoints have a public IP address and can be accessed from anywhere in the world.
 - Private endpoints exist within a virtual network and have a private IP address from within the address space of that virtual network.

#### <ins> Isolation and Segmentation </ins>

Azure virtual network allows you to crate multiple isolated virtual networks. When you set up a virtual network, 
you define a private IP address space by using either pulbic or private IP address ranges. The IP range only exists
within the virtual network and isn't internet routable. You can divide that IP address space into subnets and allocate 
part of the defined address space to each named subnet.

For name resolution, you can use the3 name resolution service that's built into Azure. You also can configure the 
virtual network to use either an internal or an external DNS server.

#### <ins> Communications <ins>

**Internet Communictations:**

You can enable incoming connections from the internet by assigning a public IP address to an Azure resource, or putting
the resource behind a public load balancer.

**Communicate between Azure resources**

You'll want to enable Azure resources to communicate securely with each other. You can do that in one of two ways:
 - Virtual networks can connect not only VMs but other Azure resources.
 - Service endpoints connect to other Azure resource types, such as Azure SQL databases and storage accounts.

**Communicate with on-premises resources**

Azure virtual networks enable you to link resources together in your on-premises environment and within your Azure
subscription. In effect, you can create a network that spans both your local and cloud environments. There are three
mechanisms for you to achieve this connectivity:
 - Point-to-site virtual private network connections are from a computer outside your organization back into your corporate
network. In this case, the client computer initiates an encrypted VPN connection to connect to the Azure virtual network.
 - Site-to-site virtual private networks link your on-premisesVPN device or gateway to the Azure VPN gateway in a virtual network.
In effect, the devices in Azure can appear as being on the local network. The connection is encrypted and works over the internet.
 - Azure ExpressRoute provides a dedicated private connectivity to Azure that doesn't travel over the internet. ExpressRoute
is useful for environments where you need greater bandwidth and even higher levels of security.

#### <ins> Route network traffic </ins>

By default, Azure routes traffic between subnets on any connected virtual networks, on-premises networks, and the internet.
You also can control routing and override those settings, as follows:
 - Route tables allow you to define rules about how traffic should be directed. You can create custom route tables that control how packets 
are routed between subnets.
 - Border Gateway Protocol (BGP) works with Azure VPN Gateways, Azure Route Server, or Azure ExpressRoute to propagate
on-premises BGP routes to Azure Virtual Networks.

#### <ins> Filter network traffic </ins>

Azure virtual networks enable you to filter traffic between subnets by using the following approaches:
 - Network security groups are Azure resources that can contain multiple inbound and outbound security rules. 
You can define there rules to allow or block traffic, based on factors such as source and destination IP address, port
and protocol.
 - Network virtual appliances are specialized VMs that can be compared to a hardened network appliance. A network 
virtual appliance carries out a particular network function, such as running a firewall or performing wide area network
 (WAN) optimization.

#### <ins> Connect virtual networks </ins>

You can link virtual networks together by using virtual network peering. Peering allows two virtual networks to connect 
directly to each other. Network traffic between peered networks is private, and travels on the Microsoft backbone network,
never entering the public internet. Peering enables resources in each virtual network to communicate with each other. 
These virtual networks can be in separate regions, which allows you to create a global interconnected network  through Azure.

User-defined routes (UDR) allow you to control the routing tables between subnets within a virtual network or between virtual
networks. This allows for greater control over network traffic flow.

### <ins> Virtual Private Networks </ins>

A virtual private network (VPN) uses an encrypted tunnel within another network. VPNs are typically deployed to connect 
two or more trusted private networks to one another over an untrusted network (typically the public internet).

#### <ins> VPN Gateways </ins>

A VPN Gateway is a type of virtual network gateway. Azure VPN Gateway instances are deployed in a dedicated subnet of the
virtual network and enable the following connectivity:
 - Connect on-premises datacenters to virtual networks through a site-to-site connection.
 - Connect individual devices to virtual networks through a point-to-site connection.
 - Connect virtual networks to other virtual networks through a network-to-network connection.

All data transfer is encrypted inside a private tunnel as it crosses the internet. You can deploy only one VPN gateway in 
each virtual network. However, you can use one gateway to connect to multiple locations, which includes other virtual 
networks or on-premises datacenters.

When setting up a VPN gateway, you must specify the type of VPN - either policy-based or route-based. The primary distinction
between these two types is how they determine which traffic needs encryption. In Azure, regardless of the VPN type, the method
of authentication employed is a pre-shared key.

 - Policy-based VPN gateways spescify statically the IP address of packets that should be encrypted through each tunnel.
 - In Route-based gateways, IPSec tunnels are modeled as a network interface or virtual tunnel interface.  
Route-based VPNs are the preferred connection method for on-premises devices.

Use route-based VPN gateway if you need any of the following types of connectivity:
 - Connections between virtual networks
 - Point-to-site connections
 - Multisite connections
 - Coexistence with an Azure ExpressRoute gateway

#### <ins> High-availability scenarios </ins>

If you're configuring a VPN to keep your information safe, you also want to be sure that it's a highly available and fault 
tolerant VPN configuration. There are a few ways to maximize the resiliency of your VPN gateway:

**Active/standby**:

By default, VPN gateways are deployed as two instances in an active/standby configuration, even if you only see one VPN
gateway resource in Azure. When planned maintenance or unplanned disruption affects the active instance, the standby 
instance automatically assumes responsibility for connections without any user intervention. Connections are interrupted 
during this failover, but they're typically restored within a few seconds for planned maintenance and within 90 seconds 
for unplanned disruptions.

**Avtive/active**

With the introduction of support for the BGP routing protocol, you can also deploy VPN gateways in an active/active 
configuration. In this configuration, you assign a unique public IP address to each instance. You then create separate 
tunnels from the on-premises device to each IP address. You can extend the high availability by deploying an additional
VPN device on-premises.

**ExpressRoute failover**

Another high-availability option is to configure a VPN gateway as a secure failover path for ExpressRoute connections.
ExpressRoute circuits have resiliency built in. However, they aren't immune to physical problems that affect the cables 
delivering connectivity or outages that affect the complete ExpressRoute location. In high-availability scenarios, where 
there's risk associated with an outage of an ExpressRoute circuit, you can also provision a VPN gateway that uses the
internet as an alternative method of connectivity. In this way, you can ensure there's always a connection to the virtual
networks.

**Zone-redundant Gateways**

In regions that support availability zones, VPN gateways and ExpressRoute gateways can be deployed in a zone-redundant 
configuration. Deploying gateways in Azure availability zones physically and logically separates gateways within a region
while protecting your on-premises network connectivity to Azure from zone-level failures. These gateways require different
gateway stock keeping units (SKUs) and use Standard public IP addresses instead of Basic public IP addresses.

### <ins> ExpressRoute </ins>

... Not even going to bother with ExpressRoute and Azure DNS for now. Read and take notes before the exam.

## <ins> 6 Storage Services </ins>

### <ins> Storage Accounts </ins>

A storage account provides a unique namespace for your Azure Storage data that's accessible from anywhere in the world
over HTTP or HTTPS. Data in this account is secure, highly available, durable and massively scalable.

When you create your storage account, you'll start by picking the storage account type. 
The type of account determines the storage services and redundancy options and has an impact on the use cases.

Redundancy Options (will be covered in detail later):
 - Locally redundant storage (LRS)
 - Geo-redundant storage (GRS)
 - Read-access geo-redundant storage (RA-GRS)
 - Zone-redundant storage (ZRS)
 - Geo-zone-redundant storage (GZRS)
 - Red-access geo-zone-redundant storage (RA-GZRS)

| Type                        | Supported Services                                                                        | Redundancy Options                   | Usage                                                                                                                                                                                                                                        |
|-----------------------------|-------------------------------------------------------------------------------------------|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Standard general-purpose v2 | Blob Storage (including Data Lake Storage), Queue Storage, Table Storage, and Azure Files | LRS, GRS, RA-GRS, ZRS, GZRS, RA-GZRS | Standard storage account type for blobs, file shares, queues, and tables. Recommended for most scenarios using Azure Storage. If you want support for network file system (NFS) in Azure Files, use the premium file shares account type.    | 
| Premium block blobs         | Blob Storage (including Data Lake Storage)                                                | LRS, ZRS                             | Premium storage account type for block blobs and append blobs. Recommended for scenarios with high transaction rates or that use smaller objects or require consistently low storage latency.                                                |
| Premium file shares         | Azure Files                                                                               | LRS, ZRS                             | Premium storage account type for file shares only. Recommended for enterprise or high-performance scale applications. Use this account type if you want a storage account that supports both Server Message Block (SMB) and NFS file shares. |
| Premium page blobs          | Page blobs only                                                                           | LRS                                  | 	Premium storage account type for page blobs only.                                                                                                                                                                                           |

#### <ins> Storage Account Endpoints </ins>

One of the benefits of using an Azure Storage Account is having a unique namespace in Azure for your data.
In order to do this, every storage account in Azure must have a unique-in-Azure account name. The combination of the account
name and the Azure Storage service endpoint forms the endpoints for your storage account.

The following table show the endpoint format for Azure Storage Services:

| Storage Service        | Endpoint                                              |
|------------------------|-------------------------------------------------------|
| Blob storage           | https://<storage-account-name>.blob.core.windows.net  |
| Data Lake Storage Gen2 | https://<storage-account-name>.dfs.core.windows.net   |
| Azure Files            | https://<storage-account-name>.file.core.windows.net  | 
| Queue Storage          | https://<storage-account-name>.queue.core.windows.net |
| Table Storage          | https://<storage-account-name>.table.core.windows.net | 

### <ins> Storage Redundancy </ins>

Azure Storage always stores multiple copies of your data so that it's protected from planned and unplanned failure events.
Redundancy ensures that your storage account meets its availability and durability targets.

When deciding which redundancy option is best for your scenario, consider the tradeoffs between lower costs and higher
availability. The factors that help determine which redundancy option you should choose include:
 - How your data is replicated in the primary region
 - Whether your data is replicated to a second region that is geographically distant to the primary region, to protect
against regional disasters.
 - Whether your application requires read access to the replicated data in the secondary region if the primary region 
becomes unavailable.

### <ins> Redundancy in the primary region </ins>

Data in an Azure Storage account is always replicated three times in the primary region. Azure Storage offers two options
for how your data is replicated in the primary region, locally redundant storage (LRS) and zone-redundant storage(ZRS).

#### <ins> Locally Redundant Storage </ins>

LRS replicates your data three times within a single data center in the primary region.
LRS provides at least a durability of 99.999999999% of objects over a given year.

<img alt="LRS diagram" src="https://learn.microsoft.com/en-us/training/wwl-azure/describe-azure-storage-services/media/locally-redundant-storage-37247957.png"/>

LRS is the lowest-cost redundancy option and offers the least durability compared to other options.
LRS protects your data against server rack and drive failures. However, if a disaster strikes the data center, all 
replicas of a storage account using LRS may be lost.

To mitigate risk, Microsoft recommends using zone-redundant storage (ZRS), geo-redundant storage (GRS) or geo-zone-redundant storage (GZRS)

#### <ins> Zone-Redundant Storage </ins>

For Availability Zone Regions, ZRS replicates your Azure Storage data synchronously across three Azure availability zones
in the primary region. ZRS provides at least a durability of 99.9999999999% of objects over a given year.

<img alt="ZRS diagram" src="https://learn.microsoft.com/en-us/training/wwl-azure/describe-azure-storage-services/media/zone-redundant-storage-6dd46d22.png"/>

With ZRS, your data is still accessible for both read and write operations even if a zone becomes unavailable.
No remounting of Azure file shares from the connected clients is required. If a zone becomes unavailable, Azure undertakes
networking updates, such as DNS repointing.

Microsoft recommends using ZRS in the primary region for scenarios that require high availability.
ZRS is also recommended for restricting replication of data within a country or region to meet data governance requirements.

#### <ins> Redundancy in a Secondary Region </ins>

https://learn.microsoft.com/en-us/training/modules/describe-azure-storage-services/3-redundancy