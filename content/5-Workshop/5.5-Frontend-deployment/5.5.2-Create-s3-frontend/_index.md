---
title: "Create S3 Frontend Bucket"
date: 2026-07-19
weight: 2
chapter: false
pre: " <b> 5.5.2. </b> "
---

## Objective

Create a private S3 bucket to store frontend static files.

## Steps

1. Create the S3 frontend bucket with the approved name `[TO BE CONFIRMED]`.
2. Enable Block Public Access.
3. Keep static website hosting disabled when using CloudFront OAC.
4. Upload the contents of `dist/`.
5. Keep bucket policy private until CloudFront OAC is configured.

```bash
aws s3 sync dist/ s3://<FRONTEND_BUCKET_NAME>/ --delete
```

![Create S3 frontend bucket](/images/5-Workshop/5.5-Frontend-deployment/create-s3-frontend-bucket.png)

## Result Checklist

- Bucket is private.
- Static files are uploaded.
- No public bucket policy is used.
