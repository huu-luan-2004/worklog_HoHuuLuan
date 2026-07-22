---
title: "Configure Route 53"
date: 2026-07-19
weight: 5
chapter: false
pre: " <b> 5.5.5. </b> "
---

## Objective

Create DNS records that point the BravelSport hostname to CloudFront.

## Steps

1. Open the Route 53 Hosted Zone for `bravelsport.com`.
2. Confirm the hostname used for the workshop `[TO BE CONFIRMED]`.
3. Create or update an Alias record that points to the CloudFront distribution.
4. Do not change production records without an approved migration plan.
5. Wait for DNS propagation and test the domain through HTTPS.

![Configure Route 53](/images/5-Workshop/5.5-Frontend-deployment/configure-route53.png)

## Result Checklist

- The DNS record points to CloudFront.
- HTTPS works with the expected certificate.
- Existing production records are not overwritten by mistake.
