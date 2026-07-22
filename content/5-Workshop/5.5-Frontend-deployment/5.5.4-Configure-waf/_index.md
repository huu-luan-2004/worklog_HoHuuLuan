---
title: "Configure AWS WAF"
date: 2026-07-19
weight: 4
chapter: false
pre: " <b> 5.5.4. </b> "
---

## Objective

Attach AWS WAF to CloudFront to inspect public HTTP/HTTPS requests.

## Steps

1. Create a Web ACL in the CloudFront scope.
2. Add baseline managed rules appropriate for the workshop.
3. Start new or risky rules in Count mode.
4. Associate the Web ACL with the CloudFront distribution.
5. Review sampled requests and metrics.
6. Move rules to Block only after false positives are reviewed.

![Configure WAF](/images/5-Workshop/5.5-Frontend-deployment/configure-waf.png)

## Result Checklist

- Web ACL is attached to CloudFront.
- WAF metrics are available.
- Rules do not block valid workshop traffic unexpectedly.
