---
title: "Create public and private subnets"
date: 2026-07-19
weight: 2
chapter: false
pre: " <b> 5.3.2. </b> "
---

## Objective

Create public and private subnets for ALB, NAT Gateway, and ECS Fargate.

## Steps

1. Create two public subnets in different Availability Zones.
2. Create two private subnets in the same Availability Zone pair.
3. Name the public subnets `bravelsport-public-a` and `bravelsport-public-b`.
4. Name the private subnets `bravelsport-private-a` and `bravelsport-private-b`.
5. Use subnet CIDR blocks from the approved parameter table.
6. Enable auto-assign public IPv4 only for public subnets if the design requires it.

![Create subnets](/images/5-Workshop/5.3-Network-infrastructure/create-subnets.png)

## Result Checklist

- Public and private subnets exist in at least two Availability Zones.
- CIDR blocks do not overlap.
- Subnets have clear names and tags.
- ECS will use private subnets only.
