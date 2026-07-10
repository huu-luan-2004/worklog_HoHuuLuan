---
title: "Week 9 Worklog"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives:
* Research AWS WAF services to secure web applications against common exploits.
* Configure Web ACLs and apply AWS Managed Rules to block threats automatically.
* Set up custom firewall rules (IP blocks, Rate-limiting, Geo-matching) and forward logging to CloudWatch/S3.
* Control and manage AWS resources centrally using tags via Console and AWS CLI.
* Implement IAM Policies using Tag Conditions (Attribute-Based Access Control - ABAC) to manage EC2 access.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - AWS WAF - Part 1: Read Introduction & Overview, create Web ACL, apply Managed Rules (Core Rule Set), configure basic web application protection | 15/06/2026 | 15/06/2026 | <https://000026.awsstudygroup.com/> |
| 3 | - AWS WAF - Part 2: Create Custom Rules (block specific IP, URI, header), Advanced Custom Rules (rate-based, geo-match, AND/OR logic), and execute rule testing | 16/06/2026 | 16/06/2026 | <https://000026.awsstudygroup.com/> |
| 4 | - AWS WAF - Part 3: Configure request logging (S3/CloudWatch), review all rules, verify testing, and cleanup resources | 17/06/2026 | 17/06/2026 | <https://000026.awsstudygroup.com/> |
| 5 | - Managing Resources with Tags - Part 1: Create and assign tags to multiple resources (EC2, S3, VPC), utilizing tags on Console & AWS CLI | 18/06/2026 | 18/06/2026 | <https://000027.awsstudygroup.com/> |
| 6 | - Managing Resources with Tags - Part 2: Create Resource Groups based on tags, manage resource grouping, review and cleanup | 19/06/2026 | 19/06/2026 | <https://000027.awsstudygroup.com/> |
| 7 | - Manage Access to EC2 with Resource Tags through IAM: Design IAM Policies with Tag conditions, create IAM Roles, execute Role switching, and verify EC2 actions across Regions (Tokyo & N.Virginia) | 20/06/2026 | 20/06/2026 | <https://000028.awsstudygroup.com/> |
| Sunday | - Total Review & Consolidation: Review all 3 labs, compare Tag strategies, clean up resources, and document best practices | 21/06/2026 | 21/06/2026 | Cả 3 link trên |

### Week 9 Achievements:
* Successfully deployed Web ACLs using AWS WAF, applying rule sets to prevent standard web threat vectors.
* Created custom rules including IP restrictions, URI matching, and rate-limiting to protect backend servers.
* Configured AWS WAF access logging to track and analyze suspicious HTTP request requests.
* Systematized AWS resource organization using resource tags and partitioned them via AWS Resource Groups.
* Built an ABAC (Attribute-Based Access Control) security model for EC2 resources via custom IAM Policies with tag matching.
* Executed comprehensive test environment teardowns to maintain cost budget objectives.
