# 🔐 30 Days of Cloud Security — Day 02

## S3 Bucket Policy Misconfig — Public Write Access

---

A public *read* bucket leaks your data.

A public *write* bucket lets someone else write to your infrastructure.

One bucket policy with `"Principal": "*"` on `s3:PutObject` — and now anyone on the internet can upload to your bucket. No IAM user. No credentials. Just:

```bash
aws s3 cp shell.php s3://target-bucket/ --no-sign-request
```

**What that actually gets an attacker:**
→ Hosting malware or phishing pages on your domain/CDN
→ Silently overwriting existing files — a cheap denial-of-service
→ Stored XSS if the bucket backs a static website
→ A foothold that looks like it came from *you*

**How to fix it:**
→ Strip `"Principal": "*"` from any write actions in your bucket policy
→ Scope write access to specific IAM roles or accounts only
→ Turn on S3 Block Public Access at the bucket and account level
→ Alert on `s3:PutBucketPolicy` calls via CloudTrail

Read access gets all the attention. Write access is the one that actually burns you.

Have you checked your bucket policies for public write, not just public read?

#CloudSecurity #AWS #S3 #CyberSecurity #DevSecOps #InfoSec
