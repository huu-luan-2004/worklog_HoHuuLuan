---
title: "Create S3 Media Bucket"
date: 2026-07-19
weight: 2
chapter: false
pre: " <b> 5.6.2. </b> "
---

## Objective

Create a private S3 bucket for media files if the workshop extends media storage from Cloudinary/local uploads to S3.

## Steps

1. Create the media bucket with an approved name `[TO BE CONFIRMED]`.
2. Enable Block Public Access.
3. Define object key prefixes for uploaded media.
4. Grant the ECS Task Role only the required S3 actions.
5. Add lifecycle rules for test data if needed.
6. Update the application configuration only after the code path is verified.

![Create S3 media bucket](/images/5-Workshop/5.6-Data-and-media/create-media-bucket.png)

## Result Checklist

- The bucket is private.
- IAM permissions are limited to the media bucket or prefix.
- The media flow is documented as implemented, planned, or `[TO BE CONFIRMED]`.
