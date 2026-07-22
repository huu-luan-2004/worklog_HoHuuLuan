---
title: "Create IAM roles for ECS"
date: 2026-07-19
weight: 3
chapter: false
pre: " <b> 5.4.3. </b> "
---

## Objective

Create separate IAM roles for ECS execution and application runtime permissions.

## Roles

### Task Execution Role

Used by ECS to pull images from ECR and send logs to CloudWatch Logs.

Typical managed policy:

- `AmazonECSTaskExecutionRolePolicy`

### Task Role

Used by the application code inside the container. Grant only the actions that the application needs, such as access to the media bucket.

## Steps

1. Create `ecsTaskExecutionRole`.
2. Attach the execution policy.
3. Create `bravelsportTaskRole`.
4. Add only required application permissions.
5. Record both ARNs in the parameter table.

![Create IAM roles](/images/5-Workshop/5.4-Backend-deployment/create-iam-roles.png)

## Result Checklist

- Execution Role and Task Role are separate.
- The Task Role does not have administrator permissions.
- No static access keys are stored in the container.
