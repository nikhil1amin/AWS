# AWS Security Project

## Introduction

The AWS Security project involved setting up a custom Virtual Private Cloud (VPC) with multiple subnets across different availability zones (AZ). The VPC was designed with a public subnet accessible via the internet through an Application Load Balancer, and a private subnet that could only be accessed from the public subnet. The public subnet contained EC2 instances with security groups to allow inbound traffic from the internet. The private subnet contained EC2 instances with security groups that only allowed traffic from the public subnet. Additional security features were implemented to restrict traffic between the subnets and limit the types of traffic that could enter or exit the VPC. Security groups were also used to restrict access to the EC2 instances to only the necessary ports and protocols.

## Project Infrastructure

The Project Infrastructure was created using the CloudFormation Service via
YAML code and few services were created via the Management
console (EC2 & ALB).


## Security Features

1. Subnet Bifurcation into Public and Private Subnets:-
The EC2 instance (Bastion Host) in the Public Subnet could be accessed
from the Internet whereas the Private Subnet instances could only be
accessed via SSH connection by the Bastion Host.

2. Application Load Balancer:-
Usage of Application Load Balancer not only to distribute the internet
traffic but also to provide availability as it connected to the EC2 instances
(Bastion Hosts) in 2 different Availability Zones. Moreover, the Security
Group of the ALB could be updated to provide access to only a particular
IP Address from the internet.
