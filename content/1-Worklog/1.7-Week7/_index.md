---
title: "Week 7 Worklog"
date: 2026-06-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives:
* Research and configure subnet-level Network ACLs to securely control Inbound/Outbound traffic.
* Establish VPC Peering Connections to connect independent VPCs, configuring routing tables and private DNS resolution.
* Study and configure Transit Gateway to aggregate multi-VPC networking based on a central Hub-and-Spoke model.
* Deploy a Serverless automation solution to start/stop EC2 instances using AWS Lambda and Amazon EventBridge (CloudWatch Events).
* Write SDK-based Lambda function code (Python/Node.js), configure IAM Roles, execute execution tests, and clean up resources (Cleanup).

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Architecture overview, prerequisites & network control configuration:<br>&emsp;+ Introduce (Overview of multi-VPC networking and security components)<br>&emsp;+ Prerequisite (Initialize 2 independent VPC networks and server resources for testing)<br>&emsp;+ Update network ACL (Configure Inbound/Outbound rules on Network ACL for subnet-level firewall control) | 8/6/2026 | 8/6/2026 | <https://000019.awsstudygroup.com/1-introduce/><br><https://000019.awsstudygroup.com/2-prerequiste/><br><https://000019.awsstudygroup.com/3-updatenetworkacl/> |
| 3 | - VPC Peering connection, routing configuration, DNS & cleanup:<br>&emsp;+ VPC Peering (Establish VPC Peering Connection between 2 independent networks)<br>&emsp;+ Route Tables (Configure Route Tables to direct packets through Peering connection)<br>&emsp;+ Cross peer DNS (Configure DNS resolution across networks to communicate via private DNS)<br>&emsp;+ Cleanup (Remove Peering connection, restore Route Tables, NACLs, and delete test VPCs) | 2/6/2026 | 3/6/2026 | <https://000019.awsstudygroup.com/4-vpcpeering/><br><https://000019.awsstudygroup.com/5-routetables/><br><https://000019.awsstudygroup.com/6-crosspeerdns/><br><https://000019.awsstudygroup.com/7-cleanup/> |
| 4 | - Solution overview, prerequisites & Transit Gateway initialization:<br>&emsp;+ Introduce (Learn Hub-and-Spoke model and Transit Gateway's role in simplifying complex VPC Peering networks)<br>&emsp;+ Prerequisite (Create component VPC networks and EC2 servers for simulation)<br>&emsp;+ Transit Gateway (Configure and initialize central Transit Gateway routing on AWS Console) | 4/6/2026 | 4/6/2026 | <https://000020.awsstudygroup.com/1-introduce/><br><https://000020.awsstudygroup.com/2-prerequiste/><br><https://000020.awsstudygroup.com/3-transitgateway/> |
| 5 | - Network system connectivity, routing configuration, result verification & cleanup:<br>&emsp;+ Transit Gateway Attachments (Connect individual VPC networks to central Transit Gateway)<br>&emsp;+ Route Table (Configure Transit Gateway and VPC routing tables)<br>&emsp;+ Result (Ping/verify connectivity between servers across different VPCs via private network)<br>&emsp;+ Cleanup (Remove Attachments, delete Transit Gateway and test VPCs) | 5/6/2026 | 5/6/2026 | <https://000020.awsstudygroup.com/4-transigatewayattachments/><br><https://000020.awsstudygroup.com/5-routetable/><br><https://000020.awsstudygroup.com/6-result/><br><https://000020.awsstudygroup.com/7-cleanup/> |
| 6 | - Architecture overview, prerequisites & system authorization configuration:<br>&emsp;+ Introduce (Learn Serverless design to automatically optimize EC2 operational costs)<br>&emsp;+ Prerequisite (Initialize EC2 servers as targets for control system)<br>&emsp;+ Create Tag for Instance (Set tagging strategy e.g. Auto-Stop to allow Lambda to identify targets)<br>&emsp;+ Create Role for Lambda (Configure IAM Role allowing Lambda to start/stop EC2 instances) | 6/6/2026 | 6/6/2026 | <https://000022.awsstudygroup.com/1-introduce/><br><https://000022.awsstudygroup.com/2-prerequiste/><br><https://000022.awsstudygroup.com/3-createtagforinstance/><br><https://000022.awsstudygroup.com/4-createroleforlambda/> |
| 7 | - Lambda function coding, automation testing & resource cleanup:<br>&emsp;+ Create Lambda Function (Create Lambda function, write source code (Python/Node.js) using SDK to start/stop EC2 based on tags)<br>&emsp;+ Testing Results (Execute test run, check logs on CloudWatch, and confirm automatic EC2 state changes)<br>&emsp;+ Cleanup (Delete Lambda function, remove IAM Role, and terminate test EC2 instances) | 8/6/2026 | 8/6/2026 | <https://000022.awsstudygroup.com/5-createlambdafunction/><br><https://000022.awsstudygroup.com/6-testingresults/><br><https://000022.awsstudygroup.com/7-cleanup/> |

### Week 7 Achievements:
* Successfully set up Network ACL rules to filter traffic at the Subnet boundary.
* Established private VPC Peering link with private DNS resolution and inter-VPC routing tables.
* Deployed Transit Gateway to route 3 component VPC networks in a Hub-and-Spoke pattern.
* Constructed serverless automations: tagged EC2 instances and granted target AWS Lambda functions IAM permissions.
* Wrote Lambda SDK code to start/stop targeted EC2 servers based on tag strategies, validating output logs.
* Removed test VPC Peering links, Transit Gateway attachments, Lambda functions, IAM roles, and target instances cleanly.
