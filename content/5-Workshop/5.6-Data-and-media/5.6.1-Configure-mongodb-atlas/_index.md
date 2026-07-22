---
title: "Configure MongoDB Atlas"
date: 2026-07-19
weight: 1
chapter: false
pre: " <b> 5.6.1. </b> "
---

## Objective

Allow ECS Fargate to connect to MongoDB Atlas safely through the NAT Gateway Elastic IP.

## Steps

1. Open MongoDB Atlas Network Access.
2. Remove temporary broad access entries if they were used during testing.
3. Add the NAT Gateway Elastic IP.
4. Create or confirm an application database user with minimum permissions.
5. Store the connection string through the approved secret mechanism `[TO BE CONFIRMED]`.
6. Test the backend connection from ECS logs and application behavior.

![Configure MongoDB Atlas](/images/5-Workshop/5.6-Data-and-media/configure-mongodb-atlas.png)

## Result Checklist

- Atlas allowlist includes the NAT Elastic IP.
- `0.0.0.0/0` is not used in production.
- Credentials are not committed to Git or shown in screenshots.
