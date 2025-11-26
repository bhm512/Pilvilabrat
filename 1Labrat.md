# IAM and Security: Lab 1 - Introduction to AWS IAM ja IAM and Security: Configure Azure Role-Based Access Control

## What was specifically done in the lab?

### AWS IAM

In this exercise:
- I logged into AWS Management Console and there worked with IAM Dashboard and Indentity components
- I created a new IAM User with programmatic and console acces
- Worked with IAM group that I created, and attached IAM Polices that needed.
- Put an IAM User to IAM Group
- Created and tested an IAM role
- Worked with security practices like: MFA, least priviledge and password polices

### Azure RBAC 

In this excercise: 
- I logged into Azure Portal
- Did some research with Azure IAM (Access Control)
- Trained with Azure AD idnetity
- Assigned a few built-in Azure roles to the user
- Changed permissions to a resource group
- Tested that assigned RBAC permissions allowed or restricted on certain actions

## Identify what cloud services you used during the lab?

### AWS

In AWS I used IAM (Identity and Access Management) and AWS Management Console

### Azure

With Azure I used Azure RBAC, Entra ID and Azure Portal 

## What technical details did you learn from the lab about each cloud services used?

### AWS

With AWS my "key" learnings would be how IAM users are humans or system identities. I also think
that knowin IAM groups are important (you can assign permissions to a multiple users at once).

Authentication vs authorization:

IAM User/Role = who you are

IAM Policy = what you can do

I it is also important to use a principle of least privilege!

### Azure

In Azure it is important to remember that RBAC is the main tool to work with roles and scopes. Also assigning to a role at higher scope inherits permissions! Unlike IAM policies with AWS, Azure RBAC uses predefined role definitions.

## Document configurations you used with each cloud services during the lab: IAM, Networking, Compute, Storage, Database, etc.

### AWS

Firstly I created user with console access (IAM user), and that purpose was to identify for login. Second step was to make a group for organizeing permissions. Third step was to attach some role-based permissions. Next step was to create role with trust to relationship to allow AWS service. Last step in this lab was to make account more safer. (Enable MFA and work with password policies)

Forgot to take pictures for this one...

### Azure RBAC

First assignment was to identify for role. Then I needed permissions for resource access. In third step I applied resource Group level (with this you can control what recources are affected). I also tested RBAC permissions in Resource Group. Lastly I attempted actions such as create resource. 

<img width="1470" height="956" alt="Näyttökuva 2025-11-18 kello 14 51 26" src="https://github.com/user-attachments/assets/2693379d-f4b7-414a-9d13-72e1fc66e19a" />

<img width="1079" height="674" alt="Näyttökuva 2025-11-18 kello 14 59 32" src="https://github.com/user-attachments/assets/cd03f614-b9e0-4d81-aae4-8622d7fe2cb6" />

<img width="1445" height="711" alt="Näyttökuva 2025-11-18 kello 15 10 24" src="https://github.com/user-attachments/assets/b8d59635-5402-4442-9071-41d0aaaaac42" />

<img width="954" height="716" alt="Näyttökuva 2025-11-18 kello 15 22 02" src="https://github.com/user-attachments/assets/52058a27-7408-4b3f-80c7-6bf1d69ed97d" />

## How AWS and Azure labs were different and similar?

First similarity between these two cloud vendors were that they both use identify based security (AWS IAM and Azure RBAC). In my opinion both were pretty similar during account creating part and assigning permissions. Last similarity was that they both (clearly) highlighted the least priviledge thing. 

The biggest difference that I caught was wiht Role and Policies, AWS IAM permissions defined with JSON policies when Azure RBAC permissions were granted by roles, assigned at certain scope. AWS IAM users exist inside AWS, when Azure Users exist in Azure AD which is whole seperate thing. 




[labclient.labondemand.com_Instructions_ExamResult_8d07cd6d-b76f-49f9-a56d-fbe38045f8bc.pdf](https://github.com/user-attachments/files/23780645/labclient.labondemand.com_Instructions_ExamResult_8d07cd6d-b76f-49f9-a56d-fbe38045f8bc.pdf)

