# 🔐 30 Days of Cloud Security — Day 01

## Public S3 Bucket Enumeration & Data Exposure

---

Most companies think their S3 buckets are private.

Most of them are wrong.

One misconfigured ACL, one public bucket policy — and your backups, logs, and customer data are sitting there for anyone to `ls`.

```bash
aws s3 ls s3://<bucket-name> --no-sign-request
```

That's it. No auth. No exploit. Just a name and a request.

**How attackers find these buckets:**
→ Guessing common naming patterns (`company-backup`, `company-prod`, `company-assets`)
→ Scraping GitHub, search engines, and cert transparency logs for leaked names
→ Automated tools — S3Scanner, bucket_finder, lazys3

**How to fix it:**
→ Enable S3 Block Public Access at the account level
→ Kill `AllUsers` / `AuthenticatedUsers` grants in your ACLs
→ Turn on AWS Config rule `s3-bucket-public-read-prohibited`
→ Run ScoutSuite or Trusted Advisor regularly

One `ls` command shouldn't be able to expose your entire data estate.

Have you ever audited your S3 buckets for public access?

#CloudSecurity #AWS #S3 #CyberSecurity #DevSecOps #InfoSec
