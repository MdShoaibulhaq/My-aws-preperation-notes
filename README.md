# My-aws-preperation-notes

**CLOUD COMPUTING**
>Cloud computing means storing and accessing data and programs over the Internet instead of your computer's hard drive.
==========================================================================
Basic Concepts of Cloud
                     There are certain services and models working behind the scene making the cloud computing feasible and accessible to end users.
 Following are the working models for cloud computing:
================================
 **Deployment Model**
======================
 ▫ Public Cloud 
▫ Private Cloud
 ▫ Hybrid Cloud
 ▫ Community Cloud
==========================================================================
**Service Models**
▫ IAAS 
▫ PAAS
 ▫ SAAS 
▫ Anything-as-a-Service (XaaS) is yet another service model, which includes Network-as-a-Service, Business-as-a-Service, Identity-as-a Service, Database-as-a-Service or Strategy-as-a-Service
==========================================================================
**Deployment Models**
========================================================================
 ▪ PUBLIC CLOUD 
The public cloud allows systems and services to be easily accessible to the general public. Public cloud may be less secure because of its openness.
==================================================================
 ▪ PRIVATE CLOUD 
The private cloud allows systems and services to be accessible within an organization. It is more secured because of its private nature.
=========================================================================
 ▪ COMMUNITY CLOUD 
The community cloud allows systems and services to be accessible by a group of organizations.
========================================================================== 
▪ HYBRID CLOUD 
The hybrid cloud is a mixture of public and private cloud, in which the critical activities are performed using private cloud while the non-critical activities are performed using public cloud.
=======================================================================
Service Models 
=====================================================================
**INFRASTRUCTURE-AS-A-SERVICE (IAAS)**
 IaaS provides access to fundamental resources such as physical machines, virtual machines, virtual storage, etc. 
==========================================================================
**PLATFORM-AS-A-SERVICE (PAAS)**
 Deploy application without managing virtual servers (Google App Engine, , AWS Elastic Beanstalk, Windows Azure, Heroku, Force.com)  and provide complete development environment, and user can easily create, test, run and deploy web applications
=========================================================================
**SOFTWARE-AS-A-SERVICE (SAAS)** 
Ready to use software applications (Gmail, Office365, Google Apps, Dropbox, Salesforce, Cisco WebEx, Concur, GoToMeeting)
==========================================================================
**AWS Global Infrastructure** ::=
==========================================================================
Amazon Cloud Computing resources are available across the world. In easy words if we see this then Amazon Data Centres are available in different geographical locations.

Organization can register their presence and launch their product using these Data Centre in any Location

AWS, in terms of its global infrastructure is broken up at the highest level between

AWS Regions
AWS Availability Zones
AWS Edge Locations
=============================================================================================
Regions
=======
Amazon Cloud Computing Resources or Data Centres are available in different Geographical Locations.

>One location is called One AWS Region.
>Each AWS Region is separate from other AWS Region.
>Availability of Services are different for different AWS Regions.
>Regions are designed to service AWS customers (or your users) that are located closest to a region.
>When viewing a region in the console you will only view resources in one region at a time.
>Availability of regions allow the architects to design applications to conform to specific laws and regulations 
>Some AWS services work "globally" while some work within a specific region only
>When we provision an EC2 instance or S3 Bucket, then you would select the region and that is where these are provisioned or stored in that region.
>One AWS region is a combination of multiple Availability Zones (AZs).
==========================================================================
Availability Zone
=========================================================================
As per AWS infrastructure, each geographical area is known as AWS Region which is a logical Data Centre. 

Each Region has multiple Physical Data Centres and these Physical Data Centres are known as AVAILABILITY ZONE or AZs.

>The Availability zone is where the actual data centres are located.
>So within a Region there can be multiple Availability zones which are physically separated but are connected through low latency and high speed internet connections.
>One Availability zone (AZ) is one Physical Data Centre.
>Each AZ has independent Power Supply, Networking, Cooling System, Physical Security.
>Each AZ connected via redundant, ultra-low-latency networks with other AZ in the same AWS Region.
>Properly designed applications will utilize multiple availability zones for High Availability and  Fault Tolerance.
>That means if any organization deploys their database in one region then the data is distributed in multiple AZs. In the issue of power outages, lightning strikes, tornadoes, earthquakes, and more at one AZ, Data is safe and accessible from other AZ.
>AZ’s are physically separated by a meaningful distance, many kilometers, from any other AZ, although all are within 100+ km (60+ miles) of each other.
=========================================================================
Region & AZ’s
======================================================================
Edge Locations
======================================================================
An Edge location can be assumed to be a collection of physical servers within a data center to allow for content distribution to reduce latency for end users. 

The higher the number of edge locations the better the content is distributed all over the world / region.

>An example would be CloudFront which is a CDN:
Cached items such as a PDF file can be cached on the edge location which reduces the amount of "space/time/latency" required for a request from the other part of the world.
		
ELASTIC COMPUTE CLOUD (EC2):-
=============================

=>Amazon Elastic Compute Cloud (Amazon EC2) provides scalable computing capacity in the Amazon Web Services (AWS) cloud.

=>Using Amazon EC2 eliminates your need to invest in hardware upfront, so you can develop and deploy applications faster.

>You can use Amazon EC2 to launch as many or as few virtual servers as you need, configure security and networking, and manage storage. Amazon EC2 enables you to scale up or down to handle changes in requirements or spikes in popularity, reducing your need to forecast traffic.
I want you to picture EC2 like a computer, and the components that make it up like OS, CPU, HDD, NW, Firewall, RAM etc.
==========================================================================
EC2 - Features
==========================================================================
=>Virtual computing environments, known as instances

=>Preconfigured templates for your instances, known as Amazon Machine Images (AMIs), that package the bits you need for your server (including the OS and additional software)

=>Various configurations of CPU, Memory, Storage and Networking capacity for your instances, known as Instance Types

=>Secure login information for your instances using Key Pairs (AWS stores the public key and you store the private key in a secure place)

=>Storage volumes for temporary data that's deleted when you stop or terminate your instance, known as Instance Store Volumes

=>The instance store is ideal for temporary storage, because the data stored in instance store volumes is not persistent through instance stops, terminations or hardware failures.

=>Persistent storage volumes for your data using Amazon Elastic Block Store, known as Amazon EBS volumes

=>A firewall that enables you to specify the protocols, ports, and source IP ranges that can reach your instances using security groups

=>Static IPv4 addresses for dynamic cloud computing, known as Elastic IP addresses
Metadata tags, that you can create and assign to your Amazon EC2 resources
Virtual networks you can create that are logically isolated from the rest of the AWS cloud known as Virtual Private Clouds (VPCs)

=========================================================================
EC2 - Configuration
=========================================================================
EC2 instances are designed to mimic traditional on-premise servers, but with the ability to be commissioned and decommissioned on-demand for easy scalability and elasticity.

>EC2 instances are primarily comprised of the follow components:
=>Amazon Machine Image (AMI): The operating system (and other softwares).
=>Instance Type: The hardware (computer power, ram, network bandwidth, etc).
=>Network interface: (public, private, or elastic IP addresses).
=>Storage: The instances "hard drive" (including two options).
=>Elastic Block Store (EBS) - which is "network persistent storage".
=>Instance Store - which is "ephemeral storage".
==========================================================================
EC2 Facts
=========================================================================
=>A Security group must be assigned to an instance during the creation process.
=>Each instance must be placed into an existing VPC, availability zone and subnet.
=>Automated (bootstrapping) custom launch commands can be passed into the instance during launch via "user - data" scripts.
=>"Tags" can be used to help name and organize provisioned instances.
=>Key-pairs are used to manage login authentication.
==========================================================================
EC2 Instance Types
==========================================================================
=>When you launch an instance, the instance type that you specify determines the hardware of the host computer used for your instance.

=>Each instance type offers different compute, memory, and storage capabilities and are grouped in instance families based on these capabilities.

=>Instances types describe the "hardware" components that an EC2 instance will run on:
Compute power (processor/vCPU)
Memory (ram)
Storage Option (hard drive)
Network Performance (bandwidth)

=>As an architect, it's important to use the proper instance type to handle your application's workload.

=>There is a collection of pre configured instance types that are grouped into families and types that you can choose from:

==========================================================================
>General Purpose Instances
==========================================================================
>General purpose instances provide a balance of compute, memory, and networking resources, and can be used for a variety of workloads.
Websites and web applications, Small and medium databases, Development, build, test, and staging environments
Check this link https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/general-purpose-instances.html
==========================================================================
Compute Optimized Instances===
==========================================================================
=> Compute optimized instances are ideal for compute-bound applications that benefit from high-performance processors. They are well suited for the following applications:
High-performance web servers, High-performance computing (HPC), Media transcoding, Scientific modeling
Check this link https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/compute-optimized-instances.html
==========================================================================
Memory Optimized Instances -
==========================================================================
==> Memory optimized instances are designed to deliver fast performance for workloads that process large data sets in memory.
High-performance, relational (MySQL) and NoSQL (MongoDB, Cassandra) databases.
In-memory databases using optimized data storage formats and analytics for business intelligence (for example, SAP HANA).
Check this link https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/memory-optimized-instances.html
=========================================================================
Storage Optimized Instances -
==========================================================================
==> Storage optimized instances are designed for workloads that require high, sequential read and write access to very large data sets on local storage. They are optimized to deliver tens of thousands of low-latency, random I/O operations per second (IOPS) to applications.
Massive parallel processing (MPP) data warehouse
MapReduce and Hadoop distributed computing
Applications that require high-throughput access to large quantities of data
Log or data processing applications
Check this link https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/storage-optimized-instances.html

========================================================================
>Accelerated Computing Instances -
===================================================================
=>If you require high processing capability, you'll benefit from using accelerated computing instances, which provide access to hardware-based compute accelerators such as Graphics Processing Units (GPUs)
Check this link https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/accelerated-computing-instances.html
=====================================================================
EC2 - Purchase Options
=========================================================================
Amazon EC2 provides the following purchasing options to enable you to optimize your costs based on your needs:
=======================================================================
On-Demand Instances – Pay, by the second, for the instances that you launch.
Savings Plans – Reduce your Amazon EC2 costs by making a commitment to a consistent amount of usage, in USD per hour, for a term of 1 or 3 years.
======================================================================
Reserved Instances – Reduce your Amazon EC2 costs by making a commitment to a consistent instance configuration, including instance type and Region, for a term of 1 or 3 years.
========================================================================
Spot Instances – Request unused EC2 instances, which can reduce your Amazon EC2 costs significantly.
==================================================================
Dedicated Hosts – Pay for a physical host that is fully dedicated to running your instances, and bring your existing per-socket, per-core, or per-VM software licenses to reduce costs.
========================================================================
Dedicated Instances – Pay, by the hour, for instances that run on single-tenant hardware.
=======================================================================
Capacity Reservations – Reserve capacity for your EC2 instances in a specific Availability Zone for any duration.
=====================================================================
Instance Lifecycle

>The lifecycle of an instance starts when it is launched and ends when it is terminated. The purchasing option that you choose affects the lifecycle of the instance. For example, an On-Demand Instance runs when you launch it and ends when you terminate it. A Spot Instance runs as long as capacity is available and your maximum price is higher than the Spot price.
========================================================================

Installing Gitbash

>Once Git Bash Windows installer is downloaded, run the executable file and follow the steps.
========
SSH
============
What is SSH & SSH Client ?
=============================================================
SSH (Secure Shell) is a network protocol that gives users, particularly system administrators, a secure way to access a remote computer. An SSH client is a program that allows establishing a secure and authenticated SSH connection to SSH servers.
Ex : Putty, GitBash, Terminal etc

SSH Syntax [ Remote Connection ]

	> ssh -i <key> username@public-ip-address

	> ssh -i <key> username@public-dns
==========================================================
EC2 Server Setup
=======================================================================
Let’s launch an instance i.e server inside AWS, using EC2 service.

Instance Setup

> Launch an Instance with Amazon Linux 2 on AWS

> Login to AWS > Services > Compute Section > EC2 > Launch Instance > Select Amazon Linux 2 AMI > Choose t2.micro > Config Instance Details {keep all default values} > Add Storage {default} > Add Tags {default} > Configure Security Group > Review & Launch > Launch Instance > In Keypair Section > Create new keypair (cst) > Launch Instance

Steps to Launch Amazon Linux 2 in AWS

> Click Services and then EC2


> Click Launch Instance


> Click AWS Marketplace
> Search for Centos
> Select Top Result - Centos7

> Click Continue

> Select your machine type and click Next Configure Instance details.
In our case we will select the t2.micro instance as it is free tier eligible.


> Leave the defaults in Configure Instance Details, Add Storage and Add Tags

> Click Next: Configure Security Group

> Click review and Launch.


> Review your settings and then click Launch.


> In the drop down menu select create a new key pair, give the key pair a name and Download the Key Pair, then click launch Instances.


> Now scroll down and click view instances

Now in order to communicate with the servers, we need an ssh client like Putty or Gitbash,

SSH Syntax
chmod 400 first.pem
ssh -i <file.pem> <username>@public-ip-address
ssh -i first.pem centos@public-ip-address
Use uname command to verify, if you get Linux, it’s successful

======================================================================
Download Putty
====================================================================
https://the.earth.li/~sgtatham/putty/latest/w64/putty.exe

Download Puttygen

https://the.earth.li/~sgtatham/putty/latest/w64/puttygen.exe

PuTTY uses .ppk files instead of .pem files. If you haven't already generated a .ppk file, do so now. For more information, see To prepare to connect to a Linux instance from Windows using PuTTY.

> Open puttygen and click Load


> Navigate to where you downloaded your key, click all files, click on your key and click open.

> Now click Save Private key, when prompted click yes you want to save without a passphrase.


> Now open putty and enter your public IP into the host name or IP address field, then expand SSH on the left had side.
> Click auth and then browse, navigate to where you saved your key and select it.

> Now click open
> Click Yes

> Enter ec2-user as the username and click enter.

> You will now be logged in

=====================================================================
>EC2 - IP Address
======================================================================
Private IP Address
=====================================================================
All EC2 instances are automatically created with a PRIVATE IP address.
The private IP address is used for internal (inside the VPC) communication between instances.
======================================================================
Public IP Address
========================================================================
=>When creating an EC2 instance, you have the option to enable (or auto-assign) a public IP address.
=>A public IP address is required if you want the EC2 instance to have direct communication with resources across the open internet, i.e if you want to directly SSH into the instance or have it directly serve web traffic.
=>Auto-assigning is based on the setting for the selected subnet that you are provisioning the instance in.
=======================================================================
Elastic IP Address (EIP)
======================================================================
=>An Elastic IP address is a public IPv4 address, which is reachable from the internet.
=>You can mask the failure of an instance or software by rapidly remapping the address to another instance in your account (i.e detaching the EIP from one instance and attaching it to another).
=>Attaching an EIP to an instance will replace it's default public IP address for as long as it is attached.
=>A disassociated Elastic IP address remains allocated to your account until you explicitly release it.
=>To ensure efficient use of Elastic IP addresses, AWS imposes a small hourly charge if an Elastic IP address is not associated with a running instance
=>An Elastic IP address is for use in a specific region only.
====================================================================

EC2 Storage
====================================================================
=>EC2 instances support two types for block level storage
Elastic Block Store - EBS (Persistent - Network attached drives)
Instance Store ( Ephemeral/temporary store)

>EC2 instances can be launched by choosing between AMIs backed by EC2 instance stores and AMIs backed by EBS. However, AWS recommends use of EBS backed AMIs, because they launch faster and use persistent storage
====================================================================
EBS - Elastic Block Store
========================================================================
=>Amazon Elastic Block Store ( Amazon EBS ) provides block level storage volumes for use with EC2 instances.

=>EBS volumes are highly available and reliable storage volumes that can be attached to any running instance that is in the same Availability Zone. EBS volumes that are attached to an EC2 instance are exposed as storage volumes that persist independently from the life of the instance. With Amazon EBS, you pay only for what you use.

=>Amazon EBS is recommended when data must be quickly accessible and requires long-term persistence. EBS volumes are particularly well-suited for use as the primary storage for file systems & databases.

Root vs Additional Volumes
=============================================================
=>Every EC2 instance must have a root volume

=>By default, EBS "root" volumes are set to be deleted when the instance is terminated. However, you can choose to have EBS volumes persist after termination.

=>You can add additional EBS volumes to instance if needed

=>Any additional volume can be attached or detached from instance at any time and is not deleted by default when instance is terminated

=>An EBS volume can attach to a single EC2 Instance only at a time

=>Both EBS Volume and EC2 instance MUST be in the same AZ


=>EBS volumes are persistent, meaning that they can live beyond the life of the EC2 instance they are attached to.

=>EBS volumes are network attached storage, meaning they can be attached/detached to or from various EC2 instances.

=>However, they can only be attached to ONE EC2 instance at a time.

>EBS volumes have the benefit of being backed up into a snapshot - which can later be restored into a new EBS volume.
=================================================================
EBS - Performance
====================================================================
EBS volumes measure input/output operations in IOPS:
IOPS are input/output operations per second
AWS measures IOPS in 256KB chunks (or smaller)
For example, A 512KB operation would count as 2 IOPS

The type of EBS volume you specify greatly influences the I/O performance (IOPS) your device

>It is important as architects to understand if your application requires more (or less) I/O when selecting an EBS volume typ
=====================================================================
EBS - Types
====================================================================
Amazon EBS provides the following volume types, which differ in performance characteristics and price, so that you can tailor your storage performance and cost to the needs of your applications. The volumes types fall into these categories:

Solid state drives (SSD) — Optimized for transactional workloads involving frequent read/write operations with small I/O size, where the dominant performance attribute is IOPS.

Hard disk drives (HDD) — Optimized for large streaming workloads where the dominant performance attribute is throughput.

Previous generation — Hard disk drives that can be used for workloads with small datasets where data is accessed infrequently and performance is not of primary importance. We recommend that you consider a current generation volume type instead.

Check the following links for more information

https://aws.amazon.com/ebs/volume-types/

>https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html
==================================================================
Instance Store
==============================================================
Instance store volumes are virtual devices whose underlying hardware is physically attached to the host computer that is running the instance.

Instance store volumes are considered ephemeral data i.e temporary storage, meaning the data on the volumes only exists for the duration of the life of the instance.

The EC2 instance attached with the instance store can't be stopped, they can only be rebooted or terminated, and termination will erase the data.

>Instance Store
Elastic Block Store
Local to Instance
Network Attached Storage
Non-persistent storage
Persistent Storage
No Snapshot Support
Point in time Snapshot support
=====================================================================
EBS - Snapshot
======================================================================
=>Frequent snapshots of your data increases data durability - so highly recommended.

=>When a snapshot is being taken against the EBS volume, it can degrade performance, so snapshots should occur during non-peak load hours

=>To take a consistent Snapshot of your non-root (not the boot) EBS Volume:
=>Pause file writes till you snapshot is complete
=>If you can't pause file writes, you need to unmount (detach) the volume from instance, take the snapshot, then re mount the volume to ensure a consistent and complete snapshot

>To create a snapshot for a root (boot) EBS Volume, you should stop the instance first then take the snapshot.
=>Be careful if you have instance store volumes on EC2 Instance , their data will be lost once you stop the instance.
===================================================================
Limitations Of EBS
=======================================================================
=>You cannot get the data across multiple availability zones
=>You cannot connect multiple instances to same EBS volume
=================================================================
AMI
====================================================================
=>An Amazon Machine Image (AMI) provides the information required to launch an instance. You must specify an AMI when you launch an instance.

=>You can launch multiple instances from a single AMI when you need multiple instances with the same configuration.

=>You can use different AMIs to launch instances when you need instances with different configurations.

=>The following diagram summarizes the AMI lifecycle. After you create and register an AMI, you can use it to launch new instances.

=>You can copy an AMI to different AWS Regions for Disaster Recovery. When you no longer require an AMI, you can deregister it.

=>You can launch an instance from an existing AMI, customize the instance (for example, install software on the instance), and then save this updated configuration as a custom AMI.

=>Instances launched from this new custom AMI include the customizations that you made when you created the AMI.

=>The root storage device of the instance determines the process you follow to create an AMI.

=>The AWS Marketplace is an online store where you can buy software that runs on AWS, including AMIs that you can use to launch your EC2 instance.

=>The AWS Marketplace AMIs are organized into categories, such as Developer Tools, to enable you to find products to suit your requirements.

=======================================================================
>Instance User Data
=====================================================================
Bootstrapping
Refers to a self-starting process i.e run set of commands without external input.
With EC2, we can bootstrap the instance (during the creation process) with custom commands (such as installing software packages, running updates and configuring other various settings).
=================================================================
User Data
===================================================================
When you launch an instance in Amazon EC2, you have the option of passing user data to the instance that can be used to perform common automated configuration tasks and even run scripts after the instance starts.

If you are familiar with shell scripting, this is the easiest and most complete way to send instructions to an instance at launch. Adding these tasks at boot time adds to the amount of time it takes to boot the instance.

You should allow a few minutes of extra time for the tasks to complete before you test that the user script has finished successfully.

User data shell scripts must start with the #! characters and the path to the interpreter you want to read the script (commonly /bin/bash).


Is data supplied by the user at instance launch in the form of a script to be executed during instance boot
User data is limited to 16KB
User data is not protected by encryption, do not include passwords or sensitive data in your user data scripts
You can change user data by stopping the instance first, then actions → Instance settings → View/Change user data

A step/section during the EC2 instance creation process where you can include your own custom commands via a script (i.e a bash script)
Here is an example of a bash script that will automate the process of updating the yum package installer, install Apache Web Server and start the Apache service.

	#!/bin/bash
	yum update -y
	yum install -y httpd
	systemctl start httpd
	systemctl enable httpd
	echo "<h1>This message from : $(hostname -i)</h1>" > /var/www/html/index.html

======================================================================
Elastic File System
======================================================================
=>EFS is a storage option for EC2 that allows for a scalable storage option.

=>EFS storage capacity is elastic.
The storage capacity will increase and decrease as you add or remove files.

=>EFS is fully managed (no maintenance required).

=>Supports the Network File system version 4.0 and 4.1 (NFSv4) protocols when mounting.

>Best performance when using an EC2 AMI with Linux kernel 4.0 or newer & EFS is not used as boot volume
=====================================================================
Benefits Of EFS
===================================================================
=>The EFS file system can be accessed by one (or more) EC2 instances at the same time
=>Shared file access across all your EC2 instances.
Applications that span multiple EC2 instances can access the same data.

=>EFS file systems can be mounted to on-premise servers ( when connected to your VPC via AWS Direct Connect).
=>This allows you to migrate data from on-premise servers to EFS and/or use it as a backup solution.

=>EFS can scale to petabytes in size, while maintaining low-latency and high levels of throughput.

=>You pay only for the amount of storage you are using.

EFS
================================================================
Amazon Elastic File System (Amazon EFS) provides a simple, scalable, fully managed elastic NFS file system.

EFS can be mounted on EC2 instances or on-premise instances through an AWS Direct connection

It is built to scale on demand to petabytes without disrupting applications, growing and shrinking automatically as you add and remove files, eliminating the need to provision and manage.

Amazon EFS can scale up to Petabyte scale, and is designed to provide massively parallel shared access to thousands of Amazon EC2 instances, enabling your applications to achieve high levels throughput.

It's limited to Linux Instances Only

You need NFS client, to mount the file system on EC2 Instances

EFS supports Network File System version 4.0 & 4.1

Multiple EC2 instances in the same region, same VPC and in different AZ's, can access amazon EFS file system at the same time.

This provides the common data source for workloads and applications running more than one instance

EFS uses port 2049 for NFS file system not for instances


EFS Mount Targets

To access EFS file system in VPC, you can create one or more mount targets in the VPC

You can create only one mount target in each availability zone

If there are multiple subnets in an AZ, you can create a mount target in one of the subnets, then all the instances in that AZ will share the mount target

Mount targets are also highly available service

>AWS recommends that you create mount targets in all the AZ's, so that you can easily mount the file system on EC2 instances that you might launch in any zone in future, as there are no charges for mount targets
============================================================
EFS Use-Cases
=============================================================
Amazon EFS enables customers to persist data from their containers and serverless functions, elastic, highly-available and high-performance, cloud-native shared file systems.

Amazon EFS allows data to be persisted separately from compute, and enables applications to have cross-AZ availability and durability.

Amazon EFS provides the ease of use, scale, performance, and consistency needed for machine learning and big data analytics workloads.  Amazon SageMaker integrates with EFS for training jobs, allowing data scientists to iterate quickly.

>Amazon EFS provides a durable, high throughput file system for content management systems and web serving applications.
=====================================================================
EFS Storage Classes
=====================================================================
Amazon EFS offers two storage classes: the Standard storage class, and the Infrequent Access storage class (EFS IA).

Standard : used to store frequently accessed data i.e daily accessed.

Infrequent Access : It's a lower cost storage class that's designed for infrequently accessed files(not accessed everyday),  IA provides cost-optimization for files not accessed every day.

>By simply enabling EFS Lifecycle Management on your file system, files not accessed according to the lifecycle policy you choose will be automatically and transparently moved into EFS IA.
============================================================================================================================================
			# AWS High Availability: Load Balancing and Auto Scaling
===========================================================================================================================================
## 1. Introduction to Elastic Load Balancer (ELB)
-------------------------------------------------
Elastic Load Balancer (ELB) is an AWS service that automatically distributes incoming application traffic across multiple targets, such as EC2 instances, containers, and IP addresses.

**Key Benefits:**
- **High Availability**: Distributes traffic across multiple targets in multiple AZs
- **Fault Tolerance**: Automatically routes traffic to healthy targets
- **Scalability**: Handles varying load by distributing traffic efficiently
- **Security**: Integrates with AWS security features like ACM, WAF, and security groups

**How ELB Works:**
1. Clients send requests to the load balancer
2. Load balancer evaluates listener rules
3. Requests are distributed to registered targets based on the routing algorithm
4. Health checks monitor target availability

## 2. Types of Load Balancers
----------------------------------------
AWS offers three types of load balancers:

### **Application Load Balancer (ALB)**
- **Layer 7 (HTTP/HTTPS)**
- Best for:
  - Web applications (HTTP/HTTPS)
  - Container-based applications
  - Microservices architectures
- Features:
  - Path-based routing
  - Host-based routing
  - Support for WebSockets and HTTP/2
  - Integration with AWS WAF

### **Network Load Balancer (NLB)**
- **Layer 4 (TCP/UDP)**
- Best for:
  - Extreme performance/low latency applications
  - TCP/UDP traffic
  - Handling volatile workloads
- Features:
  - Supports static IP addresses
  - Preserves source IP address
  - Ultra-low latency (<100ms)

### **Classic Load Balancer (CLB)**
- **Legacy option (Layer 4 & 7)**
- Best for:
  - Applications built within the EC2-Classic network
- Features:
  - Basic load balancing
  - Less configuration options than ALB/NLB
-----------------------
## 3. Target Groups
----------------------
Target groups route requests to registered targets (EC2 instances, IPs, Lambda functions).

**Key Concepts:**
- **Target Types**:
  - Instance (EC2)
  - IP (private IPs)
  - Lambda (serverless functions)
- **Health Checks**: Configure intervals, thresholds, and paths
- **Stickiness**: Route requests from same client to same target
- **Deregistration Delay**: Time to complete in-flight requests before removing target

**Best Practices:**
- Configure appropriate health check paths
- Set proper thresholds to avoid unnecessary failovers
- Use multiple target groups for complex routing
-----------------------------------------
## 4. Auto Scaling
------------------------------------------
Auto Scaling ensures you have the correct number of EC2 instances available to handle your application load.

**Key Components:**
- **Launch Template/Configuration**: Defines what to scale (AMI, instance type, etc.)
- **Scaling Policies**: When to scale (CPU utilization, request count, etc.)
- **Scaling Plans**: Maintain current instance levels at all times
- **Cooldown Period**: Time between scaling activities

**Types of Scaling:**
- **Dynamic Scaling**:
  - Target Tracking: Maintain specific metric (e.g., 70% CPU)
  - Step Scaling: Add/remove capacity in increments
  - Simple Scaling: Single adjustment per alarm
- **Predictive Scaling**: Uses machine learning to forecast traffic
- **Manual Scaling**: Set desired capacity directly

**Benefits:**
- Improved fault tolerance
- Better cost management
- Increased application availability
- 
**Vertical Scaling (Scaling Up)**
----------------------------------------
> **Vertical scaling** refers to increasing the capacity of a single server or resource by adding more power—such as CPU, RAM, or storage. It improves performance by upgrading the existing machine rather than adding more machines.

**Horizontal Scaling (Scaling Out)**
---------------------------------------------
> **Horizontal scaling** involves adding more servers or instances to a system to distribute the load. Instead of making one machine more powerful, it adds multiple machines to handle increased demand, improving availability and scalability.


# Introduction to AWS ECR (Elastic Container Registry)

In this video, we will deep dive into the fundamental concepts of ECR and provide you with a step-by-step practical guide on how to use it effectively. So, let's get started!

## Table of Contents
1. What is AWS ECR?
2. Key Benefits of ECR
3. Getting Started with AWS ECR
   - Creating an ECR Repository
   - Installing AWS CLI
   - Configuring AWS CLI
4. Pushing Docker Images to ECR
5. Pulling Docker Images from ECR
6. Cleaning Up Resources

## 1. What is AWS ECR?
AWS Elastic Container Registry (ECR) is a fully managed container image registry service provided by Amazon Web Services (AWS). It enables you to store, manage, and deploy container images (Docker images) securely, making it an essential component of your containerized application development workflow. ECR integrates seamlessly with other AWS services like Amazon Elastic Container Service (ECS) and Amazon Elastic Kubernetes Service (EKS).

## 2. Key Benefits of ECR
- **Security**: ECR offers encryption at rest, and images are stored in private repositories by default, ensuring the security of your container images.
- **Integration**: ECR integrates smoothly with AWS services like ECS and EKS, simplifying the deployment process.
- **Scalability**: As a managed service, ECR automatically scales to meet the demands of your container image storage.
- **Availability**: ECR guarantees high availability, reducing the risk of image unavailability during critical times.
- **Lifecycle Policies**: You can define lifecycle policies to automate the cleanup of unused or old container images, helping you save on storage costs.

## 3. Getting Started with AWS ECR
### Creating an ECR Repository
1. Go to the AWS Management Console and navigate to the Amazon ECR service.
2. Click on "Create repository" to create a new repository.
3. Enter a unique name for your repository and click "Create repository."

### Installing AWS CLI
To interact with ECR from your local machine, you'll need to have the AWS Command Line Interface (CLI) installed. Follow the instructions in the [AWS CLI User Guide](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-quickstart.html) to install it.

### Configuring AWS CLI
After installing the AWS CLI, open a terminal and run the following command to configure your CLI with your AWS credentials:

```
aws configure
```

Enter your AWS Access Key ID, Secret Access Key, default region, and preferred output format when prompted.

## 4. Pushing Docker Images to ECR
Now that you have your ECR repository set up and the AWS CLI configured, let's push a Docker image to ECR.

1. Build your Docker image locally using the `docker build` command:

```
docker build -t <your-image-name> <path-to-dockerfile>
```

2. Tag the image with your ECR repository URI:

```
docker tag <your-image-name>:<tag> <your-aws-account-id>.dkr.ecr.<your-region>.amazonaws.com/<your-repository-name>:<tag>
```

3. Log in to your ECR registry using the AWS CLI:

```
aws ecr get-login-password --region <your-region> | docker login --username AWS --password-stdin <your-aws-account-id>.dkr.ecr.<your-region>.amazonaws.com
```

4. Push the Docker image to ECR:

```
docker push <your-aws-account-id>.dkr.ecr.<your-region>.amazonaws.com/<your-repository-name>:<tag>
```

## 5. Pulling Docker Images from ECR
To pull and use the Docker images from ECR on another system or AWS service, follow these steps:

1. Log in to ECR using the AWS CLI as shown in Step 3 of the previous section.
2. Pull the Docker image from ECR:

```
docker pull <your-aws-account-id>.dkr.ecr.<your-region>.amazonaws.com/<your-repository-name>:<tag>
```

## 6. Cleaning Up Resources
As good practice, remember to clean up resources that you no longer need to avoid unnecessary costs. To delete an ECR repository:

1. Make sure there are no images in the repository, or delete the images using `docker rmi` locally.
2. Go to the AWS Management Console, navigate to the Amazon ECR service, and select your repository.
3. Click on "Delete" and confirm the action.


# AWS ECS Deep Dive

## Introduction

In the ever-evolving world of cloud computing, containerization has emerged as a pivotal technology, enabling developers to package their applications along with all dependencies into a single, portable unit. Amazon Elastic Container Service (ECS), a fully managed container orchestration service from AWS, simplifies the deployment, management, and scaling of containerized applications.

This blog post aims to be your ultimate guide to AWS ECS. We'll start from the fundamentals and gradually delve into the comparisons with its alternatives. We'll also discuss the pros and cons of ECS, provide step-by-step instructions for installation and configuration, and finally, guide you through deploying your first application on ECS.

## Table of Contents
1. What is AWS ECS?
2. Why Choose ECS Over Other Container Orchestration Tools?
3. ECS Fundamentals
   - Clusters
   - Task Definitions
   - Tasks
   - Services
4. Pros of Using AWS ECS
5. Cons of Using AWS ECS
6. Installation and Configuration
   - Prerequisites
   - Setting Up ECS CLI
   - Configuring AWS Credentials
7. Deploying Your First Application on ECS
   - Preparing the Application
   - Creating a Task Definition
   - Configuring the Service
   - Deploying the Service
   - Monitoring the Service
8. Conclusion

## 1. What is AWS ECS?

AWS ECS is a fully managed container orchestration service that allows you to run Docker containers at scale. It eliminates the need to manage your own container orchestration infrastructure and provides a highly scalable, reliable, and secure environment for deploying and managing your applications.

## 2. Why Choose ECS Over Other Container Orchestration Tools?

Before diving deep into ECS, let's compare it with some popular alternatives like Kubernetes and Docker Swarm.

### Comparison with Kubernetes:

Kubernetes is undoubtedly a powerful container orchestration tool with a vast ecosystem, but it comes with a steeper learning curve. ECS, on the other hand, offers a more straightforward setup and is tightly integrated with other AWS services, making it a preferred choice for AWS-centric environments.

### Comparison with Docker Swarm:

Docker Swarm is relatively easy to set up and is suitable for small to medium-scale deployments. However, as your application grows, ECS outshines Docker Swarm in terms of scalability, reliability, and seamless integration with AWS features like IAM roles and CloudWatch.

## 3. ECS Fundamentals

To understand ECS better, let's explore its core components:

### Clusters:

A cluster is a logical grouping of EC2 instances or Fargate tasks on which you run your containers. It acts as the foundation of ECS, where you can deploy your services.

### Task Definitions:

Task Definitions define how your containers should run, including the Docker image to use, CPU and memory requirements, networking, and more. It is like a blueprint for your containers.

### Tasks:

A task represents a single running instance of a task definition within a cluster. It could be a single container or multiple related containers that need to work together.

### Services:

Services help you maintain a specified number of running tasks simultaneously, ensuring high availability and load balancing for your applications.

## 4. Pros of Using AWS ECS

- **Fully Managed Service**: AWS handles the underlying infrastructure, making it easier for you to focus on deploying and managing applications.

- **Seamless Integration**: ECS seamlessly integrates with other AWS services like IAM, CloudWatch, Load Balancers, and more.

- **Scalability**: With support for Auto Scaling, ECS can automatically adjust the number of tasks based on demand.

- **Cost-Effective**: You pay only for the AWS resources you use, and you can take advantage of cost optimization features.

## 5. Cons of Using AWS ECS

- **AWS-Centric**: If you have a multi-cloud strategy or already invested heavily in another cloud provider, ECS's tight integration with AWS might be a limitation.

- **Learning Curve for Advanced Features**: While basic usage is easy, utilizing more advanced features might require a deeper understanding.

- **Limited Flexibility**: Although ECS can run non-Docker workloads with EC2 launch types, it is primarily optimized for Docker containers.

## 6. Installation and Configuration

Let's get our hands dirty and set up AWS ECS step-by-step.

### Prerequisites:

- An AWS account with appropriate IAM permissions.
- The AWS CLI and ECS CLI installed on your local machine.

### Setting Up ECS CLI:

ECS CLI is a command-line tool that simplifies the process of creating and managing ECS resources.

```bash
$ ecs-cli configure --region <region> --access-key <access-key> --secret-key <secret-key> --cluster <cluster-name>
```

### Configuring AWS Credentials:

Ensure you have the necessary AWS credentials configured using `aws configure` command.

## 7. Deploying Your First Application on ECS

In this section, we'll deploy a simple web application using ECS.

### Preparing the Application:

1. Create a Dockerfile for your web application.
2. Build the Docker image and push it to Amazon ECR (Elastic Container Registry).

### Creating a Task Definition:

Define the task using the ECS CLI or the AWS Management Console.

### Configuring the Service:

Create an ECS service to manage the desired number of tasks and set up load balancing.

### Deploying the Service:

Use the ECS CLI or the AWS Management Console to deploy the service.

### Monitoring the Service:

Monitor your ECS service using AWS CloudWatch metrics and logs.

## 8. Conclusion

In conclusion, AWS ECS offers a robust and user-friendly platform for deploying and managing containerized applications. We covered the fundamentals of ECS, compared it with its alternatives, discussed its pros and cons, and walked through the installation, configuration, and deployment of a sample application.


# AWS EKS 

## Introduction

## Table of Contents:

1. [Understanding Kubernetes Fundamentals](#understanding-kubernetes-fundamentals)
   - 1.1 [EKS vs. Self-Managed Kubernetes: Pros and Cons](#eks-vs-self-managed-kubernetes-pros-and-cons)

2. [Setting up your AWS Environment for EKS](#setting-up-your-aws-environment-for-eks)
   - 2.1 [Creating an AWS Account and Setting up IAM Users](#creating-an-aws-account-and-setting-up-iam-users)
   - 2.2 [Configuring the AWS CLI and kubectl](#configuring-the-aws-cli-and-kubectl)
   - 2.3 [Preparing Networking and Security Groups for EKS](#preparing-networking-and-security-groups-for-eks)

3. [Launching your First EKS Cluster](#launching-your-first-eks-cluster)
   - 3.1 [Using the EKS Console for Cluster Creation](#using-the-eks-console-for-cluster-creation)
   - 3.2 [Launching an EKS Cluster via AWS CLI](#launching-an-eks-cluster-via-aws-cli)
   - 3.3 [Authenticating with the EKS Cluster](#authenticating-with-the-eks-cluster)

4. [Deploying Applications on EKS](#deploying-applications-on-eks)
   - 4.1 [Containerizing Applications with Docker](#containerizing-applications-with-docker)
   - 4.2 [Writing Kubernetes Deployment YAMLs](#writing-kubernetes-deployment-yamls)
   - 4.3 [Deploying Applications to EKS: Step-by-step Guide](#deploying-applications-to-eks-step-by-step-guide)

## Understanding Kubernetes Fundamentals

### 1.1 EKS vs. Self-Managed Kubernetes: Pros and Cons

1.1.1 EKS (Amazon Elastic Kubernetes Service)
Pros:

    Managed Control Plane: EKS takes care of managing the Kubernetes control plane components, such as the API server, controller manager, and etcd. AWS handles upgrades, patches, and ensures high availability of the control plane.

    Automated Updates: EKS automatically updates the Kubernetes version, eliminating the need for manual intervention and ensuring that the cluster stays up-to-date with the latest features and security patches.

    Scalability: EKS can automatically scale the Kubernetes control plane based on demand, ensuring the cluster remains responsive as the workload increases.

    AWS Integration: EKS seamlessly integrates with various AWS services, such as AWS IAM for authentication and authorization, Amazon VPC for networking, and AWS Load Balancers for service exposure.

    Security and Compliance: EKS is designed to meet various security standards and compliance requirements, providing a secure and compliant environment for running containerized workloads.

    Monitoring and Logging: EKS integrates with AWS CloudWatch for monitoring cluster health and performance metrics, making it easier to track and troubleshoot issues.

    Ecosystem and Community: Being a managed service, EKS benefits from continuous improvement, support, and contributions from the broader Kubernetes community.

Cons:

    Cost: EKS is a managed service, and this convenience comes at a cost. Running an EKS cluster may be more expensive compared to self-managed Kubernetes, especially for large-scale deployments.

    Less Control: While EKS provides a great deal of automation, it also means that you have less control over the underlying infrastructure and some Kubernetes configurations.

1.1.2 Self-Managed Kubernetes on EC2 Instances
Pros:

    Cost-Effective: Self-managed Kubernetes allows you to take advantage of EC2 spot instances and reserved instances, potentially reducing the overall cost of running Kubernetes clusters.

    Flexibility: With self-managed Kubernetes, you have full control over the cluster's configuration and infrastructure, enabling customization and optimization for specific use cases.

    EKS-Compatible: Self-managed Kubernetes on AWS can still leverage various AWS services and features, enabling integration with existing AWS resources.

    Experimental Features: Self-managed Kubernetes allows you to experiment with the latest Kubernetes features and versions before they are officially supported by EKS.

Cons:

    Complexity: Setting up and managing a self-managed Kubernetes cluster can be complex and time-consuming, especially for those new to Kubernetes or AWS.

    Maintenance Overhead: Self-managed clusters require manual management of Kubernetes control plane updates, patches, and high availability.

    Scaling Challenges: Scaling the control plane of a self-managed cluster can be challenging, and it requires careful planning to ensure high availability during scaling events.

    Security and Compliance: Self-managed clusters may require additional effort to implement best practices for security and compliance compared to EKS, which comes with some built-in security features.

    Lack of Automation: Self-managed Kubernetes requires more manual intervention and scripting for certain operations, which can increase the risk of human error.

## Setting up your AWS Environment for EKS

Sure! Let's go into detail for each subsection:

## 2.1 Creating an AWS Account and Setting up IAM Users

Creating an AWS account is the first step to access and utilize AWS services, including Amazon Elastic Kubernetes Service (EKS). Here's a step-by-step guide to creating an AWS account and setting up IAM users:

1. **Create an AWS Account**:
   - Go to the AWS website (https://aws.amazon.com/) and click on the "Create an AWS Account" button.
   - Follow the on-screen instructions to provide your email address, password, and required account details.
   - Enter your payment information to verify your identity and set up billing.

2. **Access AWS Management Console**:
   - After creating the account, you will receive a verification email. Follow the link in the email to verify your account.
   - Log in to the AWS Management Console using your email address and password.

3. **Set up Multi-Factor Authentication (MFA)** (Optional but recommended):
   - Once you are logged in, set up MFA to add an extra layer of security to your AWS account. You can use MFA with a virtual MFA device or a hardware MFA device.

4. **Create IAM Users**:
   - Go to the IAM (Identity and Access Management) service in the AWS Management Console.
   - Click on "Users" in the left-hand navigation pane and then click on "Add user."
   - Enter a username for the new IAM user and select the access type (Programmatic access, AWS Management Console access, or both).
   - Choose the permissions for the IAM user by adding them to one or more IAM groups or attaching policies directly.
   - Optionally, set permissions boundary, tags, and enable MFA for the IAM user.

5. **Access Keys (for Programmatic Access)**:
   - If you selected "Programmatic access" during user creation, you will receive access keys (Access Key ID and Secret Access Key).
   - Store these access keys securely, as they will be used to authenticate API requests made to AWS services.

## 2.2 Configuring the AWS CLI and kubectl

With IAM users set up, you can now configure the AWS CLI and kubectl on your local machine to interact with AWS services and EKS clusters:

1. **Installing the AWS CLI**:
   - Download and install the AWS CLI on your local machine. You can find installation instructions for various operating systems [here](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-quickstart.html).

2. **Configuring AWS CLI Credentials**:
   - Open a terminal or command prompt and run the following command:
     ```
     aws configure
     ```
   - Enter the access key ID and secret access key of the IAM user you created earlier.
   - Choose a default region and output format for AWS CLI commands.

3. **Installing kubectl**:
   - Install kubectl on your local machine. Instructions can be found [here](https://kubernetes.io/docs/tasks/tools/install-kubectl/).

4. **Configuring kubectl for EKS**:
   - Once kubectl is installed, you need to configure it to work with your EKS cluster.
   - In the AWS Management Console, go to the EKS service and select your cluster.
   - Click on the "Config" button and follow the instructions to update your kubeconfig file. Alternatively, you can use the AWS CLI to update the kubeconfig file:
     ```
     aws eks update-kubeconfig --name your-cluster-name
     ```
   - Verify the configuration by running a kubectl command against your EKS cluster:
     ```
     kubectl get nodes
     ```

## 2.3 Preparing Networking and Security Groups for EKS

Before launching an EKS cluster, you need to prepare the networking and security groups to ensure proper communication and security within the cluster:

1. **Creating an Amazon VPC (Virtual Private Cloud)**:
   - Go to the AWS Management Console and navigate to the VPC service.
   - Click on "Create VPC" and enter the necessary details like VPC name, IPv4 CIDR block, and subnets.
   - Create public and private subnets to distribute resources in different availability zones.

Sure! Let's go into detail for each of the points:

2. **Configuring Security Groups**

**Security Groups** are a fundamental aspect of Amazon Web Services (AWS) that act as virtual firewalls for your AWS resources, including Amazon Elastic Kubernetes Service (EKS) clusters. Security Groups control inbound and outbound traffic to and from these resources based on rules you define. Here's a step-by-step guide on configuring Security Groups for your EKS cluster:

1. **Create a Security Group**:
   - Go to the AWS Management Console and navigate to the Amazon VPC service.
   - Click on "Security Groups" in the left-hand navigation pane.
   - Click on "Create Security Group."
   - Provide a name and description for the Security Group.
   - Select the appropriate VPC for the Security Group.

2. **Inbound Rules**:
   - Define inbound rules to control incoming traffic to your EKS worker nodes.
   - By default, all inbound traffic is denied unless you explicitly allow it.
   - Common inbound rules include allowing SSH (port 22) access for administrative purposes and allowing ingress traffic from specific CIDR blocks or Security Groups.

3. **Outbound Rules**:
   - Define outbound rules to control the traffic leaving your EKS worker nodes.
   - By default, all outbound traffic is allowed unless you explicitly deny it.
   - For security purposes, you can restrict outbound traffic to specific destinations or ports.

4. **Security Group IDs**:
   - After creating the Security Group, you'll receive a Security Group ID. This ID will be used when launching your EKS worker nodes.

5. **Attach Security Group to EKS Worker Nodes**:
   - When launching the EKS worker nodes, specify the Security Group ID in the launch configuration. This associates the Security Group with the worker nodes, allowing them to communicate based on the defined rules.

Configuring Security Groups ensures that only the necessary traffic is allowed to and from your EKS worker nodes, enhancing the security of your EKS cluster.

3. **Setting Up Internet Gateway (IGW)**

An **Internet Gateway (IGW)** is a horizontally scaled, redundant, and highly available AWS resource that allows communication between your VPC and the internet. To enable EKS worker nodes to access the internet for tasks like pulling container images, you need to set up an Internet Gateway in your VPC. Here's how to do it:

1. **Create an Internet Gateway**:
   - Go to the AWS Management Console and navigate to the Amazon VPC service.
   - Click on "Internet Gateways" in the left-hand navigation pane.
   - Click on "Create Internet Gateway."
   - Provide a name for the Internet Gateway and click "Create Internet Gateway."

2. **Attach Internet Gateway to VPC**:
   - After creating the Internet Gateway, select the Internet Gateway in the list and click on "Attach to VPC."
   - Choose the VPC to which you want to attach the Internet Gateway and click "Attach."

3. **Update Route Tables**:
   - Go to "Route Tables" in the Amazon VPC service.
   - Identify the Route Table associated with the private subnets where your EKS worker nodes will be deployed.
   - Edit the Route Table and add a route with the destination `0.0.0.0/0` (all traffic) and the Internet Gateway ID as the target.

By setting up an Internet Gateway and updating the Route Tables, you provide internet access to your EKS worker nodes, enabling them to interact with external resources like container registries and external services.

4. **Configuring IAM Policies**

**Identity and Access Management (IAM)** is a service in AWS that allows you to manage access to AWS resources securely. IAM policies define permissions that specify what actions are allowed or denied on specific AWS resources. For your EKS cluster, you'll need to configure IAM policies to grant necessary permissions to your worker nodes and other resources. Here's how to do it:

1. **Create a Custom IAM Policy**:
   - Go to the AWS Management Console and navigate to the IAM service.
   - Click on "Policies" in the left-hand navigation pane.
   - Click on "Create policy."
   - Choose "JSON" as the policy language and define the permissions required for your EKS cluster. For example, you might need permissions for EC2 instances, Auto Scaling, Elastic Load Balancing, and accessing ECR (Elastic Container Registry).

2. **Attach the IAM Policy to IAM Roles**:
   - Go to "Roles" in the IAM service and select the IAM role that your EKS worker nodes will assume.
   - Click on "Attach policies" and search for the custom IAM policy you created in the previous step.
   - Attach the policy to the IAM role.

3. **Update EKS Worker Node Launch Configuration**:
   - When launching your EKS worker nodes, specify the IAM role ARN (Amazon Resource Name) of the IAM role that includes the necessary IAM policy.
   - The IAM role allows the worker nodes to authenticate with the EKS cluster and access AWS resources based on the permissions defined in the attached IAM policy.

By configuring IAM policies and associating them with IAM roles, you grant specific permissions to your EKS worker nodes, ensuring they can interact with AWS resources as needed while maintaining security and access control.

By completing these steps, your AWS environment is ready to host an Amazon EKS cluster. You can proceed with creating an EKS cluster using the AWS Management Console or AWS CLI as described in section 3.

