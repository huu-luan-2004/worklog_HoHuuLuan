---
title: "Database and media"
date: 2026-07-19
weight: 6
chapter: false
pre: " <b> 5.6. </b> "
---

## Objective

Configure MongoDB Atlas access from ECS through NAT Gateway and document the media storage approach using S3.

## MongoDB Atlas

ECS Fargate tasks run in private subnets. Their outbound traffic reaches MongoDB Atlas through the private route table, NAT Gateway, Internet Gateway, and then Atlas.

The NAT Gateway Elastic IP must be added to the Atlas IP Access List. Do not use `0.0.0.0/0` in the final configuration.

## Media

The current source code can use Cloudinary or local `/uploads`. S3 Media is treated as a workshop extension or migration target. The final implementation should define how uploaded files are stored, read, and protected.

## Result Checklist

- Atlas access is limited to required IP addresses.
- Database credentials are not exposed.
- The S3 Media bucket is private.
- The application permission model is documented.

## Navigation

- Previous section: [5.5. Frontend deployment](../5.5-Frontend-deployment/)
- Next section: [5.7. End-to-end testing](../5.7-Testing/)
