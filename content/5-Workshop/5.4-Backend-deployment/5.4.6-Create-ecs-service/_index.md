---
title: "Create ECS service"
date: 2026-07-19
weight: 6
chapter: false
pre: " <b> 5.4.6. </b> "
---

## Objective

Create the ECS service that runs the backend tasks in private subnets and registers them with the ALB target group.

## Steps

1. Create an ECS service in `bravelsport-cluster`.
2. Use launch type Fargate.
3. Select the backend task definition.
4. Set desired count to `[TO BE CONFIRMED]`.
5. Select private subnets only.
6. Disable public IP assignment.
7. Attach the ECS security group.
8. Connect the service to `bravelsport-backend-tg`.
9. Wait until tasks are running and target health is healthy.

![Create ECS service](/images/5-Workshop/5.4-Backend-deployment/create-ecs-service.png)

## Result Checklist

- Tasks run in private subnets.
- Public IP assignment is disabled.
- Target health is healthy.
- Backend logs appear in CloudWatch Logs.
