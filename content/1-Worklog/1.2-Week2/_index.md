---
title: "Week 2 Worklog"
date: 2026-04-27
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:
* Learn and practice initializing EC2 servers (Windows & Linux), mastering the lifecycle and server management mechanisms.
* Practice SSH/RDP connections to administer systems, monitor performance, and manage EC2 costs.
* Deploy a connection architecture linking web applications (EC2) with relational databases (Amazon RDS), and perform data backups.
* Configure fault tolerance and auto-scaling mechanisms by combining Application Load Balancers (ALB) and Auto Scaling Groups (ASG).

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Architecture overview, prerequisites & EC2 server initialization:<br>&emsp;+ Introduce (Overview of EC2 practice objectives)<br>&emsp;+ Prerequisite (Configure necessary prerequisites: Key Pair, Security Group before creating server)<br>&emsp;+ Launch Windows Instance (Practice initializing virtual server running Windows OS)<br>&emsp;+ Launch Linux Instance (Practice initializing virtual server running Linux OS)<br>&emsp;+ Amazon EC2 Basic (Master basic concepts of instance state and lifecycle management) | 27/4/2026 | 27/4/2026 | <https://000004.awsstudygroup.com/1-introduce/><br><https://000004.awsstudygroup.com/2-prerequiste/><br><https://000004.awsstudygroup.com/3-launchwindowsinstance/><br><https://000004.awsstudygroup.com/4-launchlinuxinstance/><br><https://000004.awsstudygroup.com/5-amazonec2basic/> |
| 3 | - Server administration, cost control & resource cleanup:<br>&emsp;+ AWS FCJ Management - Linux (Practice administration, SSH connection, and application configuration on Linux environment)<br>&emsp;+ AWS FCJ Management - Windows (Practice RDP connection and system management on Windows environment)<br>&emsp;+ Cost Usage & Governance (Learn principles of cost governance, performance monitoring, and EC2 cost optimization)<br>&emsp;+ Cleanup (Practice terminating instances and deleting associated resources to avoid unexpected charges) | 28/4/2026 | 28/4/2026 | <https://000004.awsstudygroup.com/6-awsfcjmanagement-linux/><br><https://000004.awsstudygroup.com/7-awsfcjmanagement-windows/><br><https://000004.awsstudygroup.com/8-costusagegovernance/><br><https://000004.awsstudygroup.com/9-cleanup/> |
| 4 | - Overview, preparation & infrastructure initialization:<br>&emsp;+ Introduce (Overview of connection architecture between application and database)<br>&emsp;+ Prerequisite (Configure necessary conditions: Security Group for cross-connections, Subnet Group)<br>&emsp;+ Create EC2 (Initialize EC2 virtual server acting as Application Server to run source code)<br>&emsp;+ Create RDS (Initialize Amazon RDS relational database - MySQL/PostgreSQL acting as Database Server) | 29/4/2026 | 29/4/2026 | <https://000005.awsstudygroup.com/1-introduce/><br><https://000005.awsstudygroup.com/2-prerequiste/><br><https://000005.awsstudygroup.com/3-create-ec2/><br><https://000005.awsstudygroup.com/4-create-rds/> |
| 5 | - Application deployment, backup management & system cleanup:<br>&emsp;+ Deploy App (Practice connecting application on EC2 with RDS database and testing actual operation)<br>&emsp;+ Backup (Learn backup mechanisms, create Snapshots to protect system data)<br>&emsp;+ Cleanup (Process to clean up, delete RDS database instance and terminate EC2 server to avoid unexpected charges) | 30/4/2026 | 30/4/2026 | <https://000005.awsstudygroup.com/5-deploy-app/><br><https://000005.awsstudygroup.com/6-backup/><br><https://000005.awsstudygroup.com/7-cleanup/> |
| 6 | - Architectural overview, preparation & Load Balancing setup:<br>&emsp;+ Introduction (Overview of scaling architecture and system fault tolerance)<br>&emsp;+ Preparation (Perform network configuration and baseline resource steps)<br>&emsp;+ Create Launch Template (Practice creating configuration template for bulk server creation)<br>&emsp;+ Setup Load Balancer (Initialize and configure Load Balancer to distribute traffic) | 1/5/2026 | 1/5/2026 | <https://000006.awsstudygroup.com/1-introduction/><br><https://000006.awsstudygroup.com/2-preparation/><br><https://000006.awsstudygroup.com/3-create-launch-template/><br><https://000006.awsstudygroup.com/4-setup-load-balancer/> |
| 7 | - Auto Scaling configuration, system testing & resource cleanup:<br>&emsp;+ Test (Verify independent operation of Load Balancer before integrating scaling)<br>&emsp;+ Create Auto Scaling Group (Practice initializing ASG based on Launch Template)<br>&emsp;+ Test Solutions (Simulate overload or server failure scenarios to test auto-scaling and self-healing)<br>&emsp;+ Cleanup (Clean up process, delete ASG and Load Balancer to avoid unwanted charges) | 2/5/2026 | 2/5/2026 | <https://000006.awsstudygroup.com/5-test/><br><https://000006.awsstudygroup.com/6-create-auto-scaling-group/><br><https://000006.awsstudygroup.com/7-test-solutions/><br><https://000006.awsstudygroup.com/8-cleanup/> |

### Week 2 Achievements:
* Successfully deployed and managed Windows and Linux EC2 virtual instances.
* Established secure SSH (Linux) and RDP (Windows) administrative access, configuring services and cost limits.
* Successfully connected applications on EC2 servers to backend Amazon RDS (MySQL/PostgreSQL) databases and created backups.
* Configured an Application Load Balancer (ALB) and Auto Scaling Group (ASG) to establish system scalability and high availability.
* Verified auto-scaling, load distribution, and instance failover, completing the system cleanup to avoid costs.
