# Highly Available Web Application on AWS

##  Project Overview

This project demonstrates the design and deployment of a highly available web application architecture on Amazon Web Services (AWS).

The architecture is designed to provide high availability, security, and scalability by distributing resources across two Availability Zones.

##  Architecture

(Architecture diagram will be added here.)

##  AWS Services Used

- Amazon VPC
- Public Subnets
- Private Subnets
- Internet Gateway (IGW)
- NAT Gateway
- Bastion Host
- Amazon EC2
- Network Load Balancer (NLB)
- Security Groups
- Route Tables
- CloudWatch

##  Network Design

VPC CIDR

```
10.0.0.0/16
```

Public Subnets

```
10.0.1.0/24
10.0.2.0/24
```

Private Subnets

```
10.0.3.0/24
10.0.4.0/24
```

##  Traffic Flow

```
Internet
      │
      ▼
Internet Gateway
      │
      ▼
Network Load Balancer
      │
 ┌────┴────┐
 ▼         ▼
Web 1    Web 2
      │
      ▼
Private Database
```

##  Security

- Bastion Host is used for secure SSH access.
- Web servers are deployed behind a Network Load Balancer.
- Databases are placed in private subnets.
- NAT Gateway provides outbound internet access for private resources.

##  Screenshots

Screenshots will be added soon.

##  Lessons Learned

- AWS Networking
- High Availability
- Security Groups
- Route Tables
- Network Load Balancer
- CloudWatch Monitoring

##  Author

Ahmed Ayman Fawzy
