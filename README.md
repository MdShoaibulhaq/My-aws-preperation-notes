# My-aws-preperation-notes

CLOUD COMPUTING :-Cloud computing means storing and accessing data and programs over the Internet instead of your computer's hard drive.
==========================================================================
Basic Concepts of Cloud
                     There are certain services and models working behind the scene making the cloud computing feasible and accessible to end users.
 Following are the working models for cloud computing:
================================
 ▪ Deployment Model
======================
 ▫ Public Cloud 
▫ Private Cloud
 ▫ Hybrid Cloud
 ▫ Community Cloud
==========================================================================
 ▪ Service Models 
▫ IAAS 
▫ PAAS
 ▫ SAAS 
▫ Anything-as-a-Service (XaaS) is yet another service model, which includes Network-as-a-Service, Business-as-a-Service, Identity-as-a Service, Database-as-a-Service or Strategy-as-a-Service
==========================================================================
Deployment Models
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
▪ INFRASTRUCTURE-AS-A-SERVICE (IAAS)
 IaaS provides access to fundamental resources such as physical machines, virtual machines, virtual storage, etc. 
==========================================================================
▪ PLATFORM-AS-A-SERVICE (PAAS)
 Deploy application without managing virtual servers (Google App Engine, , AWS Elastic Beanstalk, Windows Azure, Heroku, Force.com)  and provide complete development environment, and user can easily create, test, run and deploy web applications
=========================================================================
▪ SOFTWARE-AS-A-SERVICE (SAAS) 
Ready to use software applications (Gmail, Office365, Google Apps, Dropbox, Salesforce, Cisco WebEx, Concur, GoToMeeting)
==========================================================================
AWS Global Infrastructure ::=
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

One location is called One AWS Region.
Each AWS Region is separate from other AWS Region.
Availability of Services are different for different AWS Regions.
Regions are designed to service AWS customers (or your users) that are located closest to a region.
When viewing a region in the console you will only view resources in one region at a time.
Availability of regions allow the architects to design applications to conform to specific laws and regulations 
Some AWS services work "globally" while some work within a specific region only
When we provision an EC2 instance or S3 Bucket, then you would select the region and that is where these are provisioned or stored in that region.
One AWS region is a combination of multiple Availability Zones (AZs).
==========================================================================
Availability Zone
=========================================================================
As per AWS infrastructure, each geographical area is known as AWS Region which is a logical Data Centre. 

Each Region has multiple Physical Data Centres and these Physical Data Centres are known as AVAILABILITY ZONE or AZs.

=>The Availability zone is where the actual data centres are located.
=>So within a Region there can be multiple Availability zones which are physically separated but are connected through low latency and high speed internet connections.
=>One Availability zone (AZ) is one Physical Data Centre.
=>Each AZ has independent Power Supply, Networking, Cooling System, Physical Security.
=>Each AZ connected via redundant, ultra-low-latency networks with other AZ in the same AWS Region.
=>Properly designed applications will utilize multiple availability zones for High Availability and  Fault Tolerance.
=>That means if any organization deploys their database in one region then the data is distributed in multiple AZs. In the issue of power outages, lightning strikes, tornadoes, earthquakes, and more at one AZ, Data is safe and accessible from other AZ.
=>AZ’s are physically separated by a meaningful distance, many kilometers, from any other AZ, although all are within 100+ km (60+ miles) of each other.
=========================================================================
Region & AZ’s
======================================================================
Edge Locations
======================================================================
An Edge location can be assumed to be a collection of physical servers within a data center to allow for content distribution to reduce latency for end users. 

The higher the number of edge locations the better the content is distributed all over the world / region.

An example would be CloudFront which is a CDN:
Cached items such as a PDF file can be cached on the edge location which reduces the amount of "space/time/latency" required for a request from the other part of the world.
