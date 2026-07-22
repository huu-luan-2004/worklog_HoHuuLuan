---
title: "Network infrastructure"
date: 2026-07-19
weight: 3
chapter: false
pre: " <b> 5.3. </b> "
---

## Objective

Build the network foundation for the workshop: VPC, public subnets, private subnets, Internet Gateway, NAT Gateway, route tables, and security groups.

## Target Network

- One VPC for BravelSport.
- Public subnets for the Application Load Balancer and NAT Gateway.
- Private subnets for ECS Fargate tasks.
- Internet Gateway for public subnet outbound access.
- NAT Gateway for private subnet outbound access to ECR, CloudWatch, and MongoDB Atlas.
- Security groups that restrict traffic between CloudFront, ALB, ECS, and outbound services.

## Implementation Order

1. Create the VPC.
2. Create public and private subnets across at least two Availability Zones.
3. Attach an Internet Gateway.
4. Create a NAT Gateway in a public subnet.
5. Configure public and private route tables.
6. Create security groups for ALB, ECS, and the EC2 build machine.
7. Validate that public and private routing behave as expected.

## Result Checklist

- VPC CIDR does not overlap with other networks.
- Public subnets route `0.0.0.0/0` to the Internet Gateway.
- Private subnets route outbound internet traffic through the NAT Gateway.
- ECS security group accepts inbound traffic only from the ALB security group.
- EC2 build machine does not run production traffic.

## Navigation

- Previous section: [5.2. Prerequisites](../5.2-Prerequisite/)
- Next section: [5.4. Backend deployment](../5.4-Backend-deployment/)
