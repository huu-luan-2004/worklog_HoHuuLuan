---
title: "Week 5 Worklog"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives:
* Learn central backup management with AWS Backup, configure automated backup plans, and set up status notifications.
* Run restore validation tests from recovery points and clean up resources.
* Master virtual machine (VM) migration processes using VM Import/Export tools to move images between local hypervisors and AWS.
* Package applications with Docker, verify running locally, and prepare AWS target environments (RDS, EC2).
* Build Docker Images, define multi-container deployments using Docker Compose, and launch running container workloads on EC2.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Solution overview, prerequisites & backup plan configuration:<br>&emsp;+ Introduce (Overview of centralized backup management solution using AWS Backup)<br>&emsp;+ Prerequisite (Prepare baseline resources and IAM permissions for backup service)<br>&emsp;+ Create Backup Plan (Configure automated backup plans: frequency, retention period)<br>&emsp;+ Enable Noti (Configure auto-notifications for backup job success/failure) | 18/5/2026 | 18/5/2026 | <https://000013.awsstudygroup.com/1-introduce/><br><https://000013.awsstudygroup.com/2-prerequiste/><br><https://000013.awsstudygroup.com/3-createbackupplan/><br><https://000013.awsstudygroup.com/4-enablenoti/> |
| 3 | - Recovery workflow testing & resource cleanup:<br>&emsp;+ Test Restore (Simulate data loss and restore from backups to test system readiness and integrity)<br>&emsp;+ Cleanup (Clean up backup plans, recovery points, and related resources to prevent charges) | 19/5/2026 | 19/5/2026 | <https://000013.awsstudygroup.com/5-testrestore/><br><https://000013.awsstudygroup.com/6-cleanup/> |
| 4 | - Application server deployment & VM Import practice:<br>&emsp;+ Deploy Application Server (Deploy and configure application server)<br>&emsp;+ Import VM to AWS (Migrate and convert disk image of virtual machine from local environment to Amazon EC2 Instance) | 20/5/2026 | 20/5/2026 | <https://000014.awsstudygroup.com/1-deploy-application-server/><br><https://000014.awsstudygroup.com/2-import-vm-to-aws/> |
| 5 | - VM Export practice, watching demonstration videos & resource cleanup:<br>&emsp;+ Export VM from AWS (Export EC2 instance to VM format to run offline in local infrastructure)<br>&emsp;+ Video (Watch step-by-step videos and key notes to reinforce Import/Export techniques)<br>&emsp;+ Clean up (Clean up system, delete disk image files, terminate test instances to optimize cost) | 21/5/2026 | 21/5/2026 | <https://000014.awsstudygroup.com/3-export-vm-from-aws/><br><https://000014.awsstudygroup.com/4-video/><br><https://000014.awsstudygroup.com/5-clean-up/> |
| 6 | - Architecture overview, local execution & AWS infrastructure configuration:<br>&emsp;+ Introduction (Objective and hybrid architecture of Docker and AWS Cloud)<br>&emsp;+ Deploy local (Deploy and run test application locally to verify stability) <br>&emsp;+ Preparation (Prepare network, Security Groups, and baseline resources on AWS)<br>&emsp;+ Configure RDS (Initialize and configure secure Amazon RDS database)<br>&emsp;+ Configure EC2 (Prepare EC2 virtual server for Docker environment setup) | 22/5/2026 | 22/5/2026 | <https://000015.awsstudygroup.com/1-introduce/><br><https://000015.awsstudygroup.com/2-deploy-local/><br><https://000015.awsstudygroup.com/3-preparation/><br><https://000015.awsstudygroup.com/4-configure-rds/><br><https://000015.awsstudygroup.com/5-configure-ec2/> |
| 7 | - Docker packaging, application deployment to Cloud & cleanup:<br>&emsp;+ Docker image (Write Dockerfile to package application source code into image)<br>&emsp;+ Docker compose (Use Docker Compose to systematically manage multi-containers)<br>&emsp;+ Push image (Push image to registry and deploy on EC2 server connected to RDS)<br>&emsp;+ Clean up (Clean up containers, RDS database, and EC2 instance to avoid unwanted costs) | 23/5/2026 | 23/5/2026 | <https://000015.awsstudygroup.com/6-docker-image/><br><https://000015.awsstudygroup.com/7-docker-compose/><br><https://000015.awsstudygroup.com/8-push-image/><br><https://000015.awsstudygroup.com/9-clean-up/> |

### Week 5 Achievements:
* Successfully configured AWS Backup Plans and integrated SNS alerts for backup completion status.
* Verified backup restoration workflows successfully by spinning up instances from recovery points.
* Completed VM Import tasks to deploy local virtual disks as EC2 instances and VM Export tasks to retrieve EC2 instances locally.
* Validated local multi-container environments using Docker Compose, preparing equivalent AWS network, RDS, and EC2 components.
* Built Docker images, pushed to a registry, and deployed containerized services on EC2 connected to RDS.
* Tore down containers, databases, and EC2 virtual environments to manage account budgets properly.
