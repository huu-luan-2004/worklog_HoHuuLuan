---
title: "Week 10 Worklog"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives:
* Research and configure Amazon S3 Gateway Endpoints to secure connections from a VPC without routing over the public Internet.
* Research and configure Amazon S3 Interface Endpoints (AWS PrivateLink) for secure access from simulated on-premises systems.
* Configure Route 53 Resolver (Inbound/Outbound Endpoints) to achieve hybrid private DNS resolution between on-premises and AWS.
* Apply S3 Bucket Policies to enforce traffic control, permitting bucket operations only via authorized VPC Endpoints.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Solution overview, networking architecture for S3 Endpoints, and environment prep (Prerequisites) | 22/06/2026 | 22/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - Practice creating and configuring S3 Gateway Endpoints, updating VPC Route Tables, and testing upload speeds | 23/06/2026 | 23/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - Set up simulated On-Premises environments, configure VPN/Routing parameters, and launch S3 Interface Endpoints | 24/06/2026 | 24/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - Configure cross-environment hybrid DNS resolution using Route 53 Resolver Endpoints and DNS Forwarding Rules | 25/06/2026 | 25/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - Practice verifying S3 resource access from simulated on-premises servers via AWS PrivateLink and Route 53 | 26/06/2026 | 26/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 7 | - Implement S3 Bucket Policies restricting traffic to specific endpoint IDs, execute performance reviews, and cleanup systems | 27/06/2026 | 27/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Week 10 Achievements:
* Deployed S3 Gateway Endpoints, allowing private EC2 instances in restricted subnets to upload data objects securely.
* Configured S3 Interface Endpoints, routing hybrid private traffic from simulated corporate offices to S3 buckets.
* Established a robust Hybrid DNS resolution path using Route 53 Resolver Endpoints to resolve S3 private DNS names correctly.
* Applied S3 Bucket Policies to successfully block access from sources outside the specified VPC Gateway Endpoint.
* Completed resource teardowns (deleting virtual machines, VPN configurations, Resolver endpoints, and VPCs) to control costs.
