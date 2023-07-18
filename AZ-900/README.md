# [Azure Fundamentals](https://learn.microsoft.com/en-us/certifications/resources/study-guides/AZ-900)

https://learn.microsoft.com/en-us/training/paths/azure-fundamentals-describe-azure-architecture-services/

[1 Cloud Computing](#1-cloud-computing)
 - [1.1 What is cloud computing](#what-is-cloud-computing)
 - [1.2 The shared responsibility model](#the-shared-responsibility-model)
 - [1.3 Cloud Models](#cloud-models)
 - [1.4 The Consumption Based Model](#the-consumption-based-model)  

[2 The Benefits of Using Cloud Services](#2-the-benefits-of-using-cloud-services)
 - [2.1 High Availability](#high-availability)
 - [2.2 Scalability](#scalability)
 - [2.3 Reliability](#reliability)
 - [2.4 Security and Governance](#security-and-governance)
 - [2.5 Manageability](#manageability)

[3 Cloud Service Types](#3-cloud-service-types)
 - [3.1 Infrastructure as a Service (Iaas)](#infrastructure-as-a-service)
 - [3.2 Platform as a Service (PaaS)](#platform-as-a-service)
 - [3.3 Software as a Service (SaaS)](#software-as-a-service)

[4 Core Architectural Components of Azure](#4-core-architectural-components-of-azure)



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