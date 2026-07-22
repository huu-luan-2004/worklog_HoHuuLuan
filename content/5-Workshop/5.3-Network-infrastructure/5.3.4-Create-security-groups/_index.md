---
title: "Create security groups"
date: 2026-07-19
weight: 4
chapter: false
pre: " <b> 5.3.4. </b> "
---

## Objective

Create security groups that limit traffic to the required paths only.

## Security Groups

### ALB Security Group

- Allow inbound HTTP/HTTPS from the approved source path `[TO BE CONFIRMED]`.
- Allow outbound traffic to the ECS security group on port `3000`.

### ECS Security Group

- Allow inbound port `3000` only from the ALB security group.
- Allow outbound HTTPS and database traffic required for ECR, CloudWatch, MongoDB Atlas, and S3.

### EC2 Build Machine Security Group

- If SSH is used, allow port `22` only from the administrator IP.
- Do not open port `3000` to the internet.

![Create security groups](/images/5-Workshop/5.3-Network-infrastructure/create-security-groups.png)

## Result Checklist

- ECS inbound does not allow `0.0.0.0/0`.
- The ALB is the only inbound source for backend traffic.
- EC2 is not part of the runtime path.
- Security group names and tags are clear.
