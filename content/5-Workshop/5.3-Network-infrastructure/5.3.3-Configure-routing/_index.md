---
title: "Configure Internet Gateway, NAT Gateway, and routes"
date: 2026-07-19
weight: 3
chapter: false
pre: " <b> 5.3.3. </b> "
---

## Objective

Configure routing so public resources can reach the internet and private ECS tasks can make outbound connections safely.

## Steps

1. Create and attach an Internet Gateway to `bravelsport-vpc`.
2. Allocate an Elastic IP for the NAT Gateway.
3. Create the NAT Gateway in a public subnet.
4. Create a public route table with `0.0.0.0/0` pointing to the Internet Gateway.
5. Associate public subnets with the public route table.
6. Create a private route table with `0.0.0.0/0` pointing to the NAT Gateway.
7. Associate private subnets with the private route table.
8. Record the NAT Elastic IP for MongoDB Atlas allowlisting.

![Configure routes](/images/5-Workshop/5.3-Network-infrastructure/configure-routing.png)

## Result Checklist

- Public subnets have an Internet Gateway route.
- Private subnets have a NAT Gateway route.
- NAT Gateway is in a public subnet.
- The NAT Elastic IP is documented and later added to MongoDB Atlas.
