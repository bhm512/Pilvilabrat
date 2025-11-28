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

VPC = is isolated virtual network for AWS Recources.
CIDR = Is a range of IP addresses that share common network prefix.
Public subnet = routes traffic in to the Internet Gateway.
Private subnet = no direct internet route.
Internet Gateway = is must have for instances to access internet.
Security Groups = Must explicitly allow inbound HTTP/SSH.

A NAT Gateway, is a VPC resource used to provide internet connectivity to any EC2 instances running in private subnets in the VPC without those EC2 instances needing to have a direct connection to the internet gateway.

The  lab-subnet-private1-us-east-1a private subnet has a CIDR of 10.0.1.0/24, which means that it contains all IP addresses starting with 10.0.1.x.

### Document configurations you used with each cloud services during the lab: IAM, Networking, Compute, Storage, Database, etc.




<img width="1469" height="707" alt="Näyttökuva 2025-11-28 kello 16 51 48" src="https://github.com/user-attachments/assets/7f7d8ba6-ae04-46d1-aeba-4707cb8c377c" />




<img width="1467" height="497" alt="Näyttökuva 2025-11-28 kello 17 04 08" src="https://github.com/user-attachments/assets/6548bc02-3529-4e67-95aa-d195fb0335a9" />



