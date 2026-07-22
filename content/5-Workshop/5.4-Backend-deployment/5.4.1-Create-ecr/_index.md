---
title: "Create Amazon ECR repository"
date: 2026-07-19
weight: 1
chapter: false
pre: " <b> 5.4.1. </b> "
---

## Objective

Create an Amazon ECR repository to store the BravelSport backend Docker image.

## Steps

1. Open the Amazon ECR console.
2. Create a private repository named `bravelsport-backend`.
3. Enable scan on push if available for the account.
4. Add lifecycle rules for old images if the release process requires it `[TO BE CONFIRMED]`.
5. Record the repository URI.

```bash
aws ecr describe-repositories --repository-names bravelsport-backend
```

![Create ECR repository](/images/5-Workshop/5.4-Backend-deployment/create-ecr-repository.png)

## Result Checklist

- The repository exists.
- The repository URI is recorded.
- Image scanning and lifecycle policy decisions are documented.
