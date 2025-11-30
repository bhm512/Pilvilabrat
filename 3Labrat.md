# Networking: Build your VPC and Launch a Web Server & Networking: Configure network access

## AWS 

### What was specifically done in the lab?

In this lab i trained these things:

- Created a custom Virtual Private Cloud (VPC)
- Created public and/or private subnets.
- Created a security group to allow only specific ports
- Launched an EC2 instance inside the custom VPC.
- Configured an Internet Gateway.

### Identify what cloud services you used during the lab?

I used at least these services:

- Amazon VPC
- Subnets
- Internet Gateway
- Security Groups
- EC2 instance

An Internet gateway is a VPC resource that allows communication between EC2 instances in your VPC and the Internet. 

The lab-subnet-public1-us-east-1a public subnet has a CIDR of 10.0.0.0/24, which means that it contains all IP addresses starting with 10.0.0.x. The fact the route table associated with this public subnet routes 0.0.0.0/0 network traffic to the internet gateway is what makes it a public subnet.

### What technical details did you learn from the lab about each cloud services used?

- VPC = is isolated virtual network for AWS Recources.
- CIDR = Is a range of IP addresses that share common network prefix.
- Public subnet = routes traffic in to the Internet Gateway.
- Private subnet = no direct internet route.
- Internet Gateway = is must have for instances to access internet.
- Security Groups = Must explicitly allow inbound HTTP/SSH.

A NAT Gateway, is a VPC resource used to provide internet connectivity to any EC2 instances running in private subnets in the VPC without those EC2 instances needing to have a direct connection to the internet gateway.

The lab-subnet-private1-us-east-1a private subnet has a CIDR of 10.0.1.0/24, which means that it contains all IP addresses starting with 10.0.1.x.


### Document configurations you used with each cloud services during the lab: IAM, Networking, Compute, Storage, Database, etc.

I used many configurations during this lab and here are most important ones:

- Created VPC and configured CIDR Block to 10.0.0.0/16
- Changed Public subnet to 10.0.1.0/24
- Internet Gateway -> attached it to the VPC
- In Security Groups i allowed 22 (SSH) and  allowed HTTP (80)
- EC2 -> t2.micro, Amazon Linux/Ubuntu, web server installation
  

<img width="1469" height="707" alt="Näyttökuva 2025-11-28 kello 16 51 48" src="https://github.com/user-attachments/assets/7f7d8ba6-ae04-46d1-aeba-4707cb8c377c" />


<img width="1467" height="497" alt="Näyttökuva 2025-11-28 kello 17 04 08" src="https://github.com/user-attachments/assets/6548bc02-3529-4e67-95aa-d195fb0335a9" />


## Azure

### What was specifically done in the lab?

In this practice, you can create a standalone network security group that includes the inbound and outbound network access rules you need. If you have multiple VMs that serve the same purpose, you can assign that NSG to each VM at the time you create it. This technique enables you to control network access to multiple VMs under a single, central set of rules (Azure's guidance in lab)

So I did these:

- Created an Azure Virtual Network to host compute resources.
- Configured subnets within the VNet
- Modified a Network Security Group (NSG) to implement inbound and outbound firewall rules.
- Added specific inbound access rules, such as allowing: HTTP (80)

### Identify what cloud services you used during the lab?

Services I used:

- Vnet
- Some subnets
- Network Security Groups
- Azure Virtual Machine

### What technical details did you learn from the lab about each cloud services used?

Vnets are Azure's primary private networking environment and they provide IP address management and isolation.

Network Security Groups (NSGs)

- Azure's main firewall system/mechanism

Some rules in NSG: 

- priority
- inbound/outbound
- protocol
- source/destination
- port ranges
- action allow/deny

### Document configurations you used with each cloud services during the lab: IAM, Networking, Compute, Storage, Database, etc.

I used Vnets in this practice and did some configuartions in Cloudshell. 
That is a place where you can change NSG settigns. This time I allowed inbound from port 80. 
This practice was done inside VM ofcourse. 

Here is pic before I added port 80 into it:
<img width="772" height="195" alt="Näyttökuva 2025-11-30 kello 11 58 09" src="https://github.com/user-attachments/assets/7fd021e3-6bfc-4de1-9b3e-a1f2668fb483" />

And here is after I added it:
<img width="767" height="171" alt="Näyttökuva 2025-11-30 kello 11 59 33" src="https://github.com/user-attachments/assets/48b7189a-4afc-4596-828b-a8525545406d" />


## How AWS and Azure labs were different and similar? 

Both labs were build around same topic: networking and here are some similarities between these two

Same concept = different terminology

- AWS = VPC when Azure = Vnet
- AWS = Public Subnet when Azure = Subnets
- AWS = Security Groups when Azure = Network Security Groups (NSGs)
- AWS = EC2 Instance when Azure = VM

Different: 

In internet access AWS Requires explicit Internet Gateway when Azure has Public IP that automatically configures outbound access.
Routing = AWS must edit Route Table and Azure has default route works unless custom UDR needed.
Firewalls; AWS = Security Groups only and Azure has NSG at NIC or Subnet

## How do the labs relate to the topics of the module they are associated with?

These labs totaly support the modules by network topics.

There was spots were I needed to work with Cloud Networking fundamentals in both labs. Also subnets and private vs public networks were strongly represent. 
Module teached also ho cloud networks send stuff between the subnest and internet. These things linked to routing tables and internet gateways. 
Network security is also important with databases and you should always use least priviledge in firewall rules and pay attention to inbound/outbound connectivity. 

## Create a mapping to yourself what are equivalent services and concepts between AWS and Azure.

AWS - Azure

- VPC - Vnet
- Internet Gateway - Public Ip + default route
- Security Group (SG) - Network Security Group (NSG)
- Elastic IP - Public IP Address
- EC2 Instance - VM
- EBS Volume - Azure Managed Disk

  
