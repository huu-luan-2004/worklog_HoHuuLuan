---
title: "Frontend deployment"
date: 2026-07-19
weight: 5
chapter: false
pre: " <b> 5.5. </b> "
---

## Objective

Build the React/Vite frontend, upload it to a private S3 bucket, deliver it through CloudFront, attach AWS WAF, and configure Route 53.

## Implementation Order

1. Build the frontend.
2. Create the S3 frontend bucket.
3. Create CloudFront with Origin Access Control.
4. Configure AWS WAF.
5. Configure Route 53 Alias records.

## Result Checklist

- The frontend bucket is private.
- CloudFront can read from S3 through OAC.
- `/api/*` and `/socket.io/*` route to the ALB.
- The default behavior serves static frontend files.
- DNS points users to CloudFront.

## Navigation

- Previous section: [5.4. Backend deployment](../5.4-Backend-deployment/)
- Next section: [5.6. Database and media](../5.6-Data-and-media/)
