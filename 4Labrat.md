# Intermediate Cloud Concepts: Lab 6 - Scale & Load Balance your Architecture & (Implement an Azure Load Balancer?)

## AWS

### What was specifically done in the lab?

This lab the goal was to build a scabable cloud architecture consisting of multiple compute resources behind a load balancer.
Used existing VPC environment and launched Elastic Load Balancer to distribute traffic across two or more instances.
Also had to configure Elastic Load Balancer

(This lab walks you through using the Elastic Load Balancing (ELB) and Auto Scaling services to load balance and automatically scale your infrastructure. (AWS guidance))


### Identify what cloud services you used during the lab?

- EC2
- Elastic Load Balancer 
- Auto Scaling Group (ASG)
- Amazon VPC
- Security Groups, Subnets and Internet Gateway

### What technical details did you learn from the lab about each cloud services used?

Again I used EC2 instance that runs application on scalable VM's. I also now know that this Load Balancer operates with HTTP/HTTPS and it also do these healty checks that can remove instances if they not working correctly. 

- Auto Scaling Group (ASG) = Ensures the correct number of EC2 instances are available at all times.

- Security Groups = inbound rules allowed: HTTP 80 and Outbound allowed all (default stateful rules).

### Document configurations you used with each cloud services during the lab: IAM, Networking, Compute, Storage, Database, etc.

Elastic Load Balancing automatically distributes incoming application traffic across multiple Amazon EC2 instances. It enables you to achieve fault tolerance in your applications by seamlessly providing the required amount of load balancing capacity needed to route application traffic. (AWS Guidance)

Auto Scaling helps you maintain application availability and allows you to scale your Amazon EC2 capacity out or in automatically according to conditions you define. (AWS Guidance)

- EC2 Instances - VM that runs Linux and has instance type t2.micro.
- VPC
- Internet Gateway -> attached to VPC
- Security Group -> Load Balancer’s security group allows inbound traffic on port 80 (HTTP) and The EC2 instance security group only allows traffic from the ALB, not from the internet.
- Load Balancer -> The load balancer accepts public web traffic on port 80 and The load balancer forwards traffic to a group of servers
and continuously checks which servers are healthy.
- Auto Scaling Group 

Here is security groups settings:

<img width="1412" height="549" alt="Näyttökuva 2025-11-28 kello 18 05 04" src="https://github.com/user-attachments/assets/7d6635fb-254b-4e09-a71c-0dfbb95bc45a" />

## Azure

Not available...

## How do the labs relate to the topics of the module they are associated with?

This lab showed me how to use horizontal scaling using Auto Scaling Groups. Multi-AZ design ensured redundancy which is a good thing. 
High Avaibility = Load Balancement kept the application available even if an EC2 instance failed. 

Cost Optimization = Auto scaling reduces unnecessary compute charges during low usage.



