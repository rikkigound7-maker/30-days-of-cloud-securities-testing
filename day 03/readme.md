# 🔐 30 Days of Cloud Security — Day 03

## S3 Presigned URL Abuse

---

Presigned URLs are supposed to be a *safer* way to share S3 access.

Give someone a temporary, scoped URL instead of your credentials. Sounds secure — until the implementation gets sloppy.

**Where it breaks:**
→ URLs generated with no expiry, or expiry set to days/weeks instead of minutes
→ Presigned PUT URLs that let the holder upload *any* file, not just the one intended
→ URLs leaked in logs, browser history, referrer headers, or Slack messages
→ Backend generates a presigned URL for `PutObject` but forgets to restrict `Content-Type`, letting attackers upload executable or HTML content
→ Same URL reused across users because expiry was never tied to a session

**What an attacker does with it:**
→ Grabs a leaked URL from logs/history and pulls or overwrites objects long after it should've expired
→ Uploads a web shell or phishing HTML if `PutObject` scoping is weak
→ Enumerates predictable object keys once one presigned URL pattern is known

**How to fix it:**
→ Set the shortest expiry your use case allows (minutes, not days)
→ Scope presigned URLs to exact object keys and required actions only
→ Enforce `Content-Type` and `Content-Length` conditions on presigned PUTs
→ Never log full presigned URLs — mask query params before writing to logs
→ Rotate and invalidate URLs tied to a session when that session ends

A presigned URL is a temporary key. Treat it like one.

Do you check how long your presigned URLs actually stay valid?

#CloudSecurity #AWS #S3 #CyberSecurity #DevSecOps #InfoSec
