# AWS Security Project

Project Infrastructure

The Project Infrastructure was created using the CloudFormation Service via
YAML code and few of the services were created via the Management
console (EC2 & ALB).


Security Features

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
