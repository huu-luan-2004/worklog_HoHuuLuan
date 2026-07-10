---
title: "Week 11 Worklog"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives:
* Plan the network architecture and deployment infrastructure for a production-grade project on AWS.
* Configure custom VPC environments, Security Groups, IAM Roles, and secure system access rules.
* Launch and configure Amazon RDS database instances for structured persistent application storage.
* Package applications into Docker containers and push container images to Amazon ECR repositories.
* Deploy containers to run serverless tasks on Amazon ECS (Fargate), balancing traffic via Application Load Balancers.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Plan system network architecture and drawing deployment diagrams, defining IAM role requirements | 29/06/2026 | 29/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - Configure custom VPC environments (Public/Private Subnets), Internet Gateway, NAT Gateways, and Route Tables | 30/06/2026 | 30/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - Initialize and set up Amazon RDS PostgreSQL/MySQL databases, establishing secure Security Group access controls | 01/07/2026 | 01/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - Package application source code into Docker Images, initialize Amazon ECR repositories, and push images to ECR | 02/07/2026 | 02/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - Initialize Amazon ECS Clusters, define Task Definitions configuring CPU/RAM allocations, and launch Fargate services | 03/07/2026 | 03/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 7 | - Deploy Application Load Balancers (ALBs), configure Target Groups mapping to ECS Tasks, and resolve private domains in Route 53 | 04/07/2026 | 04/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Sunday | - Write CI/CD workflows (GitHub Actions / GitLab CI) to automate compilation, packaging, and deployment to ECS services | 05/07/2026 | 05/07/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Week 11 Achievements:
* Successfully designed a secure web application infrastructure plan matching the AWS Well-Architected Framework.
* Initialized private VPC networks separated into Public Subnets (for ALB entrypoints) and Private Subnets (for ECS tasks and RDS databases).
* Deployed managed Amazon RDS instances with security access restricted to internal container services.
* Packaged and stored containerized application workloads in private Amazon ECR registries.
* Deployed serverless containers via Amazon ECS Fargate, distributing traffic through Application Load Balancers.
* Configured complete CI/CD automation pipelines for continuous deployment of backend services on code commits.
