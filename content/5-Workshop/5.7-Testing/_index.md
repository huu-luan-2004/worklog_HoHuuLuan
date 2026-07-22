---
title: "End-to-end testing"
date: 2026-07-19
weight: 7
chapter: false
pre: " <b> 5.7. </b> "
---

## Objective

Verify that the deployed system works from the user entry point through CloudFront, ALB, ECS Fargate, MongoDB Atlas, and media storage.

## Test Cases

1. Open the domain through HTTPS.
2. Confirm that static frontend assets load from CloudFront.
3. Test API requests through `/api/*`.
4. Test Socket.IO through `/socket.io/*` and namespace `/chat`.
5. Confirm ECS target health is healthy.
6. Review CloudWatch Logs for backend errors.
7. Confirm MongoDB Atlas connection from the backend.
8. Test media upload or document why it remains `[TO BE CONFIRMED]`.

![End-to-end testing](/images/5-Workshop/5.7-Testing/end-to-end-testing.png)

## Result Checklist

- The website loads through CloudFront.
- API calls return expected responses.
- Realtime chat connects successfully or the issue is documented.
- ECS tasks stay healthy.
- Logs do not contain secrets.
- Test evidence is captured with sensitive values hidden.

## Navigation

- Previous section: [5.6. Database and media](../5.6-Data-and-media/)
- Next section: [5.8. Security and cost](../5.8-Security-and-cost/)
