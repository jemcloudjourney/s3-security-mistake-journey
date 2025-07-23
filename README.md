# 🔓 My First Cloud Security Mistake: Public S3 Bucket

> ⚠️ **Newbie Alert:** I'm learning cloud security in public!  
> **Start Date:** 2024-08-15  

## 🚨 The Horror Story
**What I did:**
```terraform
# vulnerable-s3.tf
resource "aws_s3_bucket" "logs" {
  bucket = "super-secret-logs"
  acl    = "public-read" # 😱 TERRIBLE IDEA!
}
