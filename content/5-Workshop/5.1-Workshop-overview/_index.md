---
title: "Workshop overview"
date: 2026-07-19
weight: 1
chapter: false
pre: " <b> 5.1. </b> "
---

## Objective

Introduce the project, technology stack, target architecture, and workshop scope. This section also clarifies the difference between the EC2 build machine and the ECS Fargate production runtime.

## BravelSport Introduction

BravelSport is an e-commerce and sports field booking platform at `https://bravelsport.com/`. The system supports product browsing, cart, orders, field booking, account management, and realtime chat.

Reference source code: `https://github.com/huu-luan-2004/ShopBanDoAo`.

Main technologies:

- Frontend: React, Vite, TypeScript.
- Backend: NestJS, TypeScript.
- Database: MongoDB through Mongoose.
- Authentication: JWT.
- Realtime: Socket.IO.
- REST API path: `/api/*`.
- Socket.IO transport path: `/socket.io/*`.
- Socket.IO namespace: `/chat`.
- Default backend port: `3000`.
- Initial health check path: `/`.
- Backend packaging: Docker.

![BravelSport homepage](/images/5-Workshop/5.1-Workshop-overview/bravelsport-homepage.jpg)

## Workshop Goals

After the workshop, the implementer can:

1. Design a VPC with public and private subnets across two Availability Zones.
2. Use an EC2 Ubuntu instance as a build and deployment machine.
3. Build the backend Docker image, push it to ECR, and run it on ECS Fargate.
4. Deploy the React/Vite frontend to a private S3 bucket and deliver it with CloudFront OAC.
5. Route `/api/*` and `/socket.io/*` from CloudFront to the ALB.
6. Connect ECS to MongoDB Atlas through NAT Gateway.
7. Send container logs to CloudWatch Logs.
8. Extend media handling from Cloudinary/local `/uploads` to S3 Media.
9. Test the system, review security, monitor cost, and clean up resources.

## Three-Layer Architecture

| Layer | Components | Role |
|---|---|---|
| Presentation | Route 53, CloudFront, WAF, S3 Frontend | DNS, TLS, static frontend delivery, and request filtering |
| Application | ALB, `ip` Target Group, ECS Fargate | Run REST API and Socket.IO on port `3000` |
| Data | MongoDB Atlas, S3 Media | Store business data and media files |

## EC2 Build Machine Role

The EC2 Ubuntu instance belongs to the Development and Deployment area. It is used to clone the source code, install tools, build the frontend, build the Docker image, log in to ECR, push the image, and run AWS CLI deployment commands.

```text
GitHub
  -> EC2 Ubuntu Build Machine
       -> build frontend -> S3 Frontend Bucket
       -> docker build -> Amazon ECR -> ECS Fargate pulls image
```

EC2 does not receive user traffic, is not attached behind the ALB, and does not run the production backend.

![Build and deployment flow](/images/5-Workshop/5.1-Workshop-overview/deployment-flow.jpg)

## ECS Fargate Role

ECS Fargate is the runtime for the NestJS backend. Each task runs a container on port `3000`, stays in a private subnet, has no public IP, and only accepts inbound traffic from the ALB security group through an `ip` target group.

## Traffic Flows

- Frontend: `User -> Route 53 -> CloudFront + AWS WAF -> S3 Frontend Bucket`
- REST API: `User -> Route 53 -> CloudFront -> /api/* -> ALB -> Target Group (ip) -> ECS Fargate:3000`
- Socket.IO: `User -> CloudFront -> /socket.io/* -> ALB -> ECS Fargate -> namespace /chat`
- MongoDB Atlas: `ECS Fargate -> Private Route Table -> NAT Gateway -> Internet Gateway -> MongoDB Atlas`
- Deployment: `GitHub -> EC2 Build Machine -> ECR -> ECS Fargate`

![BravelSport AWS Architecture](/images/5-Workshop/architecture/bravelsport-aws-architecture.png)

## Result Checklist

- The diagram does not show `ALB -> EC2`.
- Users do not access EC2, NAT Gateway, Internet Gateway, or ECS directly.
- CloudFront has separate behaviors for `/api/*` and `/socket.io/*`.
- The target group type is `ip`.
- MongoDB Atlas is outside the VPC.

## Navigation

- Previous section: [Workshop](../)
- Next section: [5.2. Prerequisites](../5.2-Prerequisite/)
