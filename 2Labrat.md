# Lab 3 - Introduction to Amazon EC2 & Create an Azure Virtual Machine

## AWS Lab 

### What was specifically done in the lab?

This is what i did in this lab:

- Used AWS Management Console
- Launched new EC2 Instance -> by using AMI
- Selected instance type and configured other detalis
- Created key pair for SSH authentication
- Trained with security group thing (indound/outbound)
- Stopped and started instance

### Identify what cloud services you used during the lab?

I used Amazon EC2, VPC and security groups in this lab. I also visited IAM protocols for permissions and roles, and practiced EBS.

### What technical details did you learn from the lab about each cloud services used?

I think i learned more about EC2 than other services but here is what is know: 

- EC2 is virtual server in AWS and it is highly scabable
- AMI's are used for virtual OS and system configuration
- Instance types define CPU and RAM for example
- These EC2 VM's can be connected via SSH or even RDP

  Other services:

  - Subnets represent IP address ranges.
  - Security groups act as stateful firewalls controlling traffic.
  - IAM policies define least-privilege access.
 
### Document configurations you used with each cloud services during the lab: IAM, Networking, Compute, Storage, Database, etc

- AMI: Amazon Linux/Ubuntu, Instance type: t2.micro (EC2 instance)
- Auto-assigned public IP, default VPC, public subnet (VPC)
- Inbound: SSH port 22 allowed only to my IP (security)
- 8–30 GB gp2/gp3 root volume (storage i think)
- Created RSA key pair for SSH login (security/key pair)


## Azure

### What was specifically done in the lab?

This is what I did in this lab:

- Logged into Azure Portal
- Created new VM
- Selected image (ubuntu)

### Identify what cloud services you used during the lab?

I used these:

- Azure Virtual Machine/VM
- Azure Virtual Network
- Cloud Shell inside VM

  Here is few screenshots about those commands i used in cloud shell:

<img width="1009" height="204" alt="Näyttökuva 2025-11-28 kello 14 27 48" src="https://github.com/user-attachments/assets/ce4f1c9e-027c-4ec0-8f79-0d0a4da619ea" />


<img width="1001" height="306" alt="Näyttökuva 2025-11-28 kello 14 26 53" src="https://github.com/user-attachments/assets/6c9c7091-dbd6-4ef1-8423-89995ca6d44c" />


### What technical details did you learn from the lab about each cloud services used?

Azure VM's can determine CPU, RAM and extensions can install software automatically. I also red that VNets are software-defined networks with subnets and Azure Managed Disks provide persistent storage for VMs.


### Document configurations you used with each cloud services during the lab: IAM, Networking, Compute, Storage, Database, etc.

I think the most important configuration were on VM's cloud shell (pictures are Identify what cloud services you used during the lab?- section) Those were critical to complete this lab exercise. Without those this lab was pretty quick to do (exept I had to wait several minutes that cloud shell started)

I used: 

- VM configuartion -> Ubuntu image
- Resource Group -> --resource-group myRGKV-lod57132629 \
- key pair -> --generate-ssh-keys

## Write a comparison between AWS and Azure laboratories for each indicated laboratory pair.

## How AWS and Azure labs were different and similar?

How AWS and Azure were similar:

- Both involved launching a virtual machine in the cloud.
- Required choosing an OS image and instance/VM size.
- Included storage configuration (EBS vs Managed Disk).

How they were different: 

- AWS EC2 uses a step-by-step wizard with explicit networking and storage details when Azure VM groups everything inside a Resource Group, making lifecycle management easier.
- AWS uses Key Pairs stored locally when Azure uses SSH Public Keys uploaded to VM or passwords.
- AWS has: EBS volumes and Azure has: Managed Disks

### How do the labs relate to the topics of the module they are associated with?

These things were on module topics:

- Cloud compute fundamentals
- Virtual networking
- Cloud storage
- Identity and access control
- Virtualization

### Create a mapping to yourself what are equivalent services and concepts between AWS and Azure.

 - EC2 = Azure Virtual Machine
 - VPC = Virtual Network
 - Security Groups = NSG (Network Security Group)
 - S3 = Blob Storage
 - IAM Users = Azure AD Users
 - IAM Roles = Role Assingment
 - Policies = Role Definions
  
<img width="658" height="256" alt="Näyttökuva 2025-11-28 kello 15 00 04" src="https://github.com/user-attachments/assets/0f017930-20f1-437e-a176-773fdcc9ad27" />



