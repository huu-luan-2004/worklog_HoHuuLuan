---
title: "Create Target Group and Application Load Balancer"
date: 2026-07-19
weight: 4
chapter: false
pre: " <b> 5.4.4. </b> "
---

## Objective

Create the Application Load Balancer and target group used by ECS Fargate.

## Steps

1. Create a target group named `bravelsport-backend-tg`.
2. Choose target type `ip`.
3. Use protocol HTTP and port `3000` unless the application design confirms another port.
4. Configure the health check path as `/` or the confirmed health endpoint.
5. Create an internet-facing ALB in public subnets.
6. Attach the ALB security group.
7. Create listener rules that forward backend traffic to the target group.

![Create ALB](/images/5-Workshop/5.4-Backend-deployment/create-alb.png)

## Result Checklist

- Target group type is `ip`.
- ALB is in public subnets.
- ECS tasks will be registered by private IP.
- Health check path is verified.
