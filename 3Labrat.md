




In this task, you will use the VPC and more option in the VPC console to create multiple resources, including a VPC, an Internet Gateway, a public subnet and a private subnet in a single Availability Zone, two route tables, and a NAT Gateway.


An Internet gateway is a VPC resource that allows communication between EC2 instances in your VPC and the Internet. 

The lab-subnet-public1-us-east-1a public subnet has a CIDR of 10.0.0.0/24, which means that it contains all IP addresses starting with 10.0.0.x. The fact the route table associated with this public subnet routes 0.0.0.0/0 network traffic to the internet gateway is what makes it a public subnet.

A NAT Gateway, is a VPC resource used to provide internet connectivity to any EC2 instances running in private subnets in the VPC without those EC2 instances needing to have a direct connection to the internet gateway.

The  lab-subnet-private1-us-east-1a private subnet has a CIDR of 10.0.1.0/24, which means that it contains all IP addresses starting with 10.0.1.x.

