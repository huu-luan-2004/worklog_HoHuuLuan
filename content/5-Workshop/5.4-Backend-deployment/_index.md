---
title: "Backend deployment"
date: 2026-07-19
weight: 4
chapter: false
pre: " <b> 5.4. </b> "
---

## Objective

Package the NestJS backend as a Docker image, push it to Amazon ECR, and run it on ECS Fargate behind an Application Load Balancer.

## Main Components

- Amazon ECR repository for the backend image.
- IAM execution role and task role.
- CloudWatch Log Group for container logs.
- Application Load Balancer and `ip` target group.
- ECS cluster, task definition, and service.

## Implementation Order

1. Create the ECR repository.
2. Build and push the backend Docker image.
3. Create IAM roles for ECS.
4. Create the ALB and target group.
5. Create the ECS cluster and task definition.
6. Create the ECS service and verify that tasks become healthy.

## Result Checklist

- The backend image is stored in ECR.
- ECS tasks run in private subnets.
- The target group type is `ip`.
- Container logs are available in CloudWatch Logs.
- The ALB forwards traffic to healthy ECS tasks.

## Navigation

- Previous section: [5.3. Network infrastructure](../5.3-Network-infrastructure/)
- Next section: [5.5. Frontend deployment](../5.5-Frontend-deployment/)
