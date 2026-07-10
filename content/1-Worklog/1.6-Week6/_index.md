---
title: "Week 6 Worklog"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:
* Learn serverless container architecture with Amazon ECS, initialize ECS Clusters, register service discovery in Cloud Map, and configure Task Definitions.
* Set up Application Load Balancers (ALB) to route microservices and spin up ECS Services.
* Study and build automated CI/CD integration/deployment pipelines utilizing GitLab CI/CD, GitHub Actions, and AWS CodeBuild.
* Implement deep container telemetry with CloudWatch Container Insights and configure log routing using AWS FireLens and Fluent Bit.
* Examine cloud security benchmarks (CIS, PCI DSS), enable AWS Security Hub, and analyze account Security Scores.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Environment preparation, ECS Cluster initialization & Task Definition configuration:<br>&emsp;+ Introduction & Preparation (Understand Amazon ECS architecture and prepare network, IAM permissions)<br>&emsp;+ Prepare for deployment (Inspect container resources before deploying to cloud)<br>&emsp;+ Register namespace in CloudMap (Register Service Discovery with AWS Cloud Map)<br>&emsp;+ Create ECS Cluster (Initialize logical ECS cluster for container applications)<br>&emsp;+ Create task definition (Define hardware allocation, environment variables, and Docker Image for container) | 25/5/2026 | 25/5/2026 | <https://000016.awsstudygroup.com/1-introduction/><br><https://000016.awsstudygroup.com/2-preparation/><br><https://000016.awsstudygroup.com/3-prepare-for-deployment/><br><https://000016.awsstudygroup.com/4-register-namespace-in-cloudmap/><br><https://000016.awsstudygroup.com/5-create-ecs-cluster/><br><https://000016.awsstudygroup.com/6-create-task-definition/> |
| 3 | - Load Balancer configuration, ECS service launch, testing & cleanup:<br>&emsp;+ Configure ALB (Set up Application Load Balancer to route external traffic)<br>&emsp;+ Create ECS Services (Run and maintain configured number of container tasks)<br>&emsp;+ Test result (Access via ALB DNS to check microservices operation)<br>&emsp;+ Clean up (Remove ECS Services, ALB, Cloud Map, and Cluster to optimize costs) | 26/5/2026 | 26/5/2026 | <https://000016.awsstudygroup.com/7-configure-alb/><br><https://000016.awsstudygroup.com/8-create-ecs-services/><br><https://000016.awsstudygroup.com/9-test-result/><br><https://000016.awsstudygroup.com/10-clean-up/> |
| 4 | - Architecture overview, preparation & CI/CD automation practice:<br>&emsp;+ Introduction & Preparation (Learn CI/CD mindset and prepare environment, permissions)<br>&emsp;+ CICD GitLab (Write configurations to build pipeline for automatic image packaging and push from GitLab)<br>&emsp;+ CICD GitHub (Build similar automation pipeline using GitHub Actions)<br>&emsp;+ CICD CodeBuild (Use AWS CodeBuild service to optimize build performance in the cloud) | 27/5/2026 | 27/5/2026 | <https://000017.awsstudygroup.com/1-introduction/><br><https://000017.awsstudygroup.com/2-preparation/><br><https://000017.awsstudygroup.com/3-cicd-gitlab/><br><https://000017.awsstudygroup.com/4-cicd-github/><br><https://000017.awsstudygroup.com/5-cicd-codebuild/> |
| 5 | - Deep container monitoring, advanced log routing & cleanup:<br>&emsp;+ Monitoring with Container Insights (Enable collection of detailed metrics using CloudWatch Container Insights)<br>&emsp;+ Logs router with FireLens (Use AWS FireLens with Fluent Bit to filter and route logs from container to targets)<br>&emsp;+ Clean up (Delete pipeline, disable log routing and Container Insights to secure account and optimize cost) | 28/5/2026 | 28/5/2026 | <https://000017.awsstudygroup.com/6-monitoring-with-container-insights/><br><https://000017.awsstudygroup.com/7-logs-router-with-firelens/><br><https://000017.awsstudygroup.com/8-clean-up/> |
| 6 | - Security standards overview & AWS Security Hub enablement:<br>&emsp;+ Security standards (Learn common cloud security standards like AWS Foundations Benchmark, CIS, PCI DSS)<br>&emsp;+ Enable sec hub (Enable AWS Security Hub on the account and collect security data) | 29/5/2026 | 29/5/2026 | <https://000018.awsstudygroup.com/1-security-standards/><br><https://000018.awsstudygroup.com/2-enable-sec-hub/> |
| 7 | - Security score analysis, configuration optimization & system cleanup:<br>&emsp;+ Security score (Analyze security score in dashboard, identify vulnerabilities/misconfigurations to fix)<br>&emsp;+ Cleanup (Disable AWS Security Hub, delete test configurations, reset account state to avoid unwanted costs) | 30/5/2026 | 30/5/2026 | <https://000018.awsstudygroup.com/3-security-score/><br><https://000018.awsstudygroup.com/4-cleanup/> |

### Week 6 Achievements:
* Launched ECS clusters, mapped Task Definitions, and established Service Discovery using AWS Cloud Map.
* Deployed Application Load Balancers to balance traffic across ECS task containers.
* Programmed operational pipelines to auto-compile and push images using GitLab CI, GitHub Actions, and AWS CodeBuild.
* Successfully gathered detailed metrics using Container Insights and routed container logs via FireLens.
* Enabled AWS Security Hub, reviewed CIS/PCI DSS compliance scoring, and completed the workspace cleanup.
