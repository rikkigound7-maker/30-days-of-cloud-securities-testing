# ☁️ 30 Days of Cloud Security

A 30-day LinkedIn series covering real-world AWS, Azure, and GCP misconfigurations — one attack technique a day, across storage, IAM, secrets, and container security.

## 📋 Overview

| | |
|---|---|
| **Duration** | 30 days |
| **Categories** | 4 |
| **Cloud Providers** | AWS, Azure, GCP |
| **Format** | Technique + exploitation context + fix, one per day |

## 🗓️ Full Checklist

### Week 1 — Storage Misconfigurations (Day 1–8)
- [ ] Day 01 — Public S3 bucket enumeration & data exposure
- [ ] Day 02 — S3 bucket policy misconfig (public write access)
- [ ] Day 03 — S3 presigned URL abuse
- [ ] Day 04 — Azure Blob Storage public container leaks
- [ ] Day 05 — GCP Cloud Storage bucket misconfig
- [ ] Day 06 — Exposed `.git` / `.env` files via cloud storage
- [ ] Day 07 — CDN / CloudFront origin exposure
- [ ] Day 08 — Terraform state file leaks (S3 backend)

### Week 2 — IAM & Privilege Escalation (Day 9–16)
- [ ] Day 09 — AWS IAM wildcard permission abuse
- [ ] Day 10 — IAM role assumption abuse (`sts:AssumeRole`)
- [ ] Day 11 — EC2 instance metadata service (IMDSv1) SSRF → credential theft
- [ ] Day 12 — Lambda over-permissioned execution roles
- [ ] Day 13 — Cross-account role trust misconfig
- [ ] Day 14 — Azure AD app registration privilege escalation
- [ ] Day 15 — GCP service account impersonation
- [ ] Day 16 — GCP overly permissive IAM bindings (Owner/Editor)

### Week 3 — Secrets Exposure (Day 17–22)
- [ ] Day 17 — AWS Secrets Manager public access misconfig
- [ ] Day 18 — Hardcoded secrets in Lambda env variables
- [ ] Day 19 — Exposed API keys in public repos tied to cloud accounts
- [ ] Day 20 — Kubernetes secrets stored in plaintext
- [ ] Day 21 — Docker image layer secret leakage
- [ ] Day 22 — CI/CD pipeline secret exposure (GitHub Actions / Jenkins)

### Week 4 — Container & Cluster Escape (Day 23–30)
- [ ] Day 23 — Container escape via privileged containers
- [ ] Day 24 — Docker socket exposure (`docker.sock` mount)
- [ ] Day 25 — Kubernetes RBAC misconfig — cluster-admin abuse
- [ ] Day 26 — Pod security policy bypass
- [ ] Day 27 — Node compromise via kubelet API (EKS/AKS/GKE)
- [ ] Day 28 — Serverless function injection (Lambda/Azure Functions)
- [ ] Day 29 — Cloud misconfig scanning tools (ScoutSuite, Prowler, CloudSploit)
- [ ] Day 30 — Recap + build-your-own cloud security checklist

## 📦 Deliverables per Day
- 1 LinkedIn post (technical, short, ends with a question + hashtags)
- 1 card image (1200×628 PNG, design system: dot grid, dark terminal block, two-column layout)

## 🏷️ Suggested Hashtags
`#CloudSecurity` `#AWS` `#Azure` `#GCP` `#CyberSecurity` `#DevSecOps` `#InfoSec`
---

> **Best posting time:** Tuesday–Thursday, 8–10 AM IST
