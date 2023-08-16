# [Azure Fundamentals](https://learn.microsoft.com/en-us/certifications/resources/study-guides/AZ-900)

https://learn.microsoft.com/en-us/training/paths/azure-fundamentals-describe-azure-architecture-services/

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
 - [4.3 Compute and Networking Services](#ins-compute-and-networking-services-ins)

## <ins>1 Cloud Computing</ins>

### <ins>Learning Goals</ins>

 - Define cloud computing
 - Describe the shared responsibility model
 - Define cloud models, including public, private and hybrid
 - Identify appropriate use cases for each cloud model
 - Describe the consumption-based model
 - Compare cloud pricing models

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

### <ins>Learning goals</ins>
 - Describe the benefits of high availability in the cloud
 - Describe the benefits of reliability and predictability in the cloud
 - Describe the benefits of security and governance in the cloud
 - Describe the benefits of manageability in the cloud

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

### <ins>Learning Goals</ins>
 - Describe infrastructure as a service (IaaS). 
 - Describe platform as a service (PaaS). 
 - Describe software as a service (SaaS). 
 - Identify appropriate use cases for each cloud service (IaaS, PaaS, SaaS).

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

### <ins> Compute and Networking Services </ins>

You are here: https://learn.microsoft.com/en-us/training/modules/describe-azure-compute-networking-services/