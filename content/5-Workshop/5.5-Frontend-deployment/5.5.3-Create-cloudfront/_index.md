---
title: "Create CloudFront Distribution"
date: 2026-07-19
weight: 3
chapter: false
pre: " <b> 5.5.3. </b> "
---

## Objective

Create a CloudFront distribution to deliver the frontend and route API traffic to the ALB.

## Steps

1. Create an Origin Access Control for the S3 frontend bucket.
2. Add the S3 bucket as the default origin.
3. Add the ALB as a custom origin for backend paths.
4. Configure default behavior for static frontend files.
5. Add behavior `/api/*` to forward requests to the ALB.
6. Add behavior `/socket.io/*` to forward websocket transport traffic to the ALB.
7. Attach the ACM certificate from `us-east-1`.
8. Update the S3 bucket policy to allow only the CloudFront distribution.

![Create CloudFront](/images/5-Workshop/5.5-Frontend-deployment/create-cloudfront.png)

## Result Checklist

- S3 is protected by OAC.
- Backend behaviors point to the ALB.
- CloudFront supports HTTPS.
- SPA routing behavior is tested if the frontend requires it.
