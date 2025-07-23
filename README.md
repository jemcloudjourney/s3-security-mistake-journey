# vulnerable-s3.tf
resource "aws_s3_bucket" "logs" {
  bucket = "super-secret-logs"
  acl    = "public-read" # 😱 TERRIBLE IDEA!
}
