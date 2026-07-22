---
title: "Prerequisites"
date: 2026-07-19
weight: 2
chapter: false
pre: " <b> 5.2. </b> "
---

## Objective

Prepare the AWS account, IAM identity, EC2 Ubuntu build machine, local tools, source code, MongoDB Atlas, DNS, certificate, and parameter table before creating AWS resources.

## Implementation Steps

### 1. Prepare the AWS account and IAM identity

- Do not use the root user for daily work.
- Create or use an IAM identity with permissions appropriate for the workshop.
- Enable MFA if possible.
- Attach an IAM role through an instance profile for EC2 instead of storing long-term access keys.
- Avoid `AdministratorAccess` when a narrower policy can be used.

Check the identity from EC2:

```bash
aws sts get-caller-identity
```

### 2. Choose the AWS Region

Choose the Region for VPC, EC2, ECR, ECS, ALB, S3 Media, and CloudWatch: `[TO BE CONFIRMED]`.

The certificate used by CloudFront must be created or imported in `us-east-1`.

### 3. Create the EC2 Ubuntu build machine

Requirements:

- Instance type: `[TO BE CONFIRMED]`.
- Storage: `[TO BE CONFIRMED]`.
- IAM instance profile with minimum permissions for ECR push, S3 upload, and deployment commands.
- Do not open port `3000`.
- If SSH is used, open port `22` only from the administrator IP `[TO BE CONFIRMED]`.
- Prefer Systems Manager Session Manager when the account and AMI support it.

![EC2 Build Machine running](/images/5-Workshop/5.2-Prerequisite/ec2-running.jpg)

### 4. Install tools

```bash
sudo apt update
sudo apt install -y git unzip ca-certificates curl

aws --version
docker --version
node --version
npm --version
git --version
```

Install the Node.js version required by `package.json` and confirm that the Docker daemon is running.

![Verify local tools](/images/5-Workshop/5.2-Prerequisite/verify-local-tools.jpg)

### 5. Clone the source code

```bash
git clone https://github.com/huu-luan-2004/ShopBanDoAo.git
cd ShopBanDoAo
git rev-parse --short HEAD
```

### 6. Test the frontend build

```bash
cd Fronted
npm ci
npm run build
ls -la dist
```

Do not put secrets in variables prefixed with `VITE_`, because those values can be bundled into static frontend files.

### 7. Test the backend Docker image

```bash
cd ../backend-nestjs
docker build -t bravelsport-backend:local .
docker image ls bravelsport-backend
```

```bash
docker run --rm -p 3000:3000 \
  --env-file <SAFE_ENV_FILE> \
  bravelsport-backend:local
```

```bash
curl -i http://localhost:3000/
```

The initial health endpoint is `/`. If the application does not return `200`, confirm the real route before creating the target group.

![Docker image build success](/images/5-Workshop/5.2-Prerequisite/backend-docker-build-success.jpg)

### 8. Prepare MongoDB Atlas

- Create a cluster.
- Create a dedicated database user with minimum permissions.
- Do not use `0.0.0.0/0` in the final configuration.
- After the NAT Gateway exists, add the NAT Elastic IP to the Atlas IP Access List.
- Do not expose the connection string in screenshots or documentation.

![MongoDB Atlas Network Access](/images/5-Workshop/5.2-Prerequisite/mongodb-network-access.jpg)

### 9. Prepare Route 53 Hosted Zone

Confirm the Hosted Zone for `bravelsport.com`. Do not change production records without a migration plan.

![Route 53 Hosted Zone](/images/5-Workshop/5.2-Prerequisite/route53-hosted-zone.jpg)

### 10. Prepare ACM certificate

In `us-east-1`, request the certificate for the hostname used by CloudFront. Complete DNS validation and wait for the status `Issued`.

![ACM certificate Issued](/images/5-Workshop/5.2-Prerequisite/acm-certificate-issued.jpg)

## Result Checklist

- `aws sts get-caller-identity` works.
- Docker daemon is running.
- `npm run build` creates the `dist/` folder.
- The backend Docker image runs and listens on port `3000`.
- The health path `/` is checked or marked for confirmation.
- Hosted Zone and ACM certificate are ready.
- No secrets appear in terminal output, screenshots, or Git history.

## Navigation

- Previous section: [5.1. Workshop overview](../5.1-Workshop-overview/)
- Next section: [5.3. Network infrastructure](../5.3-Network-infrastructure/)
