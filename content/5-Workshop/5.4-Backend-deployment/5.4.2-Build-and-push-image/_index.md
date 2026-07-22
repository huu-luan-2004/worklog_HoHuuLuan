---
title: "Build and push Docker image"
date: 2026-07-19
weight: 2
chapter: false
pre: " <b> 5.4.2. </b> "
---

## Objective

Build the backend Docker image on the EC2 build machine and push it to Amazon ECR.

## Steps

1. Log in to ECR.
2. Build the backend image.
3. Tag the image with the ECR repository URI.
4. Push the image.
5. Confirm that the image appears in ECR.

```bash
aws ecr get-login-password --region <REGION> | docker login --username AWS --password-stdin <ACCOUNT_ID>.dkr.ecr.<REGION>.amazonaws.com
docker build -t bravelsport-backend:latest .
docker tag bravelsport-backend:latest <ACCOUNT_ID>.dkr.ecr.<REGION>.amazonaws.com/bravelsport-backend:latest
docker push <ACCOUNT_ID>.dkr.ecr.<REGION>.amazonaws.com/bravelsport-backend:latest
```

Do not paste the real Account ID into screenshots or public documentation.

![Build and push image](/images/5-Workshop/5.4-Backend-deployment/build-and-push-image.png)

## Result Checklist

- Docker build finishes successfully.
- The image is pushed to ECR.
- The tag used by the ECS task definition is recorded.
