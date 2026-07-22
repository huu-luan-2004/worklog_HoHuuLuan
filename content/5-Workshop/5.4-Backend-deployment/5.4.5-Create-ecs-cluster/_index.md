---
title: "Create ECS cluster and task definition"
date: 2026-07-19
weight: 5
chapter: false
pre: " <b> 5.4.5. </b> "
---

## Objective

Create the ECS cluster, CloudWatch Log Group, and task definition for the backend.

## Steps

1. Create an ECS cluster named `bravelsport-cluster`.
2. Create a CloudWatch Log Group for backend logs.
3. Create a Fargate task definition.
4. Set CPU and memory values to `[TO BE CONFIRMED]`.
5. Set container port `3000`.
6. Use the ECR image URI created earlier.
7. Attach the Task Execution Role and Task Role.
8. Configure environment variables and secrets through the approved mechanism `[TO BE CONFIRMED]`.

![Create ECS cluster](/images/5-Workshop/5.4-Backend-deployment/create-ecs-cluster.png)

## Result Checklist

- The cluster exists.
- The task definition references the correct ECR image.
- Logs are sent to CloudWatch Logs.
- Secrets are not hardcoded in the task definition text.
