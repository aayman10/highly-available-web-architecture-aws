# Highly Available Web Application on AWS

##  Project Overview

This project demonstrates the design and deployment of a highly available web application architecture on AWS.

The architecture is distributed across two Availability Zones to improve availability and reduce the impact of a single point of failure.

The infrastructure was implemented manually using the AWS Management Console.

##  Architecture

![AWS Architecture](Architecture/Web_architecture.png)

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

# 📸 AWS Infrastructure Screenshots

## 1. Public Subnet 1

![Public Subnet 1](screenshots/01-public-subnet-1.png)

## 2. Public Subnet 2

![Public Subnet 2](screenshots/02-public-subnet-2.png)

## 3. Private Subnet 1

![Private Subnet 1](screenshots/03-private-subnet-1.png)

## 4. Private Subnet 2

![Private Subnet 2](screenshots/04-private-subnet-2.png)

## 5. Internet Gateway

![Internet Gateway](screenshots/05-IGW.png)

## 6. NAT Gateway

![NAT Gateway](screenshots/06-NAT-Gateway.png)

## 7. Bastion Host

![Bastion Host](screenshots/07-Bastion-EC2.png)

## 8. Web Server 1

![Web Server 1](screenshots/08-WEB-Server-1-EC2.png)

## 9. Web Server 2

![Web Server 2](screenshots/09-WEB-Server-2-EC2.png)

## 10. Database Server 1

![Database Server 1](screenshots/10-WEB-DB-1-EC2.png)

## 11. Database Server 2

![Database Server 2](screenshots/11-WEB-DB-2-EC2.png)

## 12. Web Server Launch Template

![Web Server Launch Template](screenshots/12-WEBserver-template.png)

## 13. Web Server 2 Launch Template

![Web Server 2 Launch Template](screenshots/13-WEBserver2-template.png)

## 14. Network Load Balancer

![Network Load Balancer](screenshots/14-NLB.png)

## 15. Bastion Security Group

![Bastion Security Group](screenshots/15-WEB-Bastion_Sg.png)

## 16. Web Application Security Group

![Web Application Security Group](screenshots/16-WEB-AppServer_Sg.png)

## 17. Database Security Group

![Database Security Group](screenshots/17-WEB-DB_Sg.png)

## 18. Public NACL

![Public NACL](screenshots/18-Pub-NACL.png)

## 19. Private NACL

![Private NACL](screenshots/19-Priv-NACL.png)

## 20. CloudWatch

![CloudWatch](screenshots/20-CloudWatch.png)

##  Lessons Learned

- AWS Networking
- High Availability
- Security Groups
- Route Tables
- Network Load Balancer
- CloudWatch Monitoring

##  Author

Ahmed Ayman Fawzy
