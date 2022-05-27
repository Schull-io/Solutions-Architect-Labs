# Task 2: Create Amazon S3 bucket with bucket policies and life cycle management

1. Launch AWS Console
2. Create a S3 bucket with enforced ownership
3. Create a single lifecycle policy
seye3-rule
Edit
Delete

Actions
Lifecycle rule configuration
Lifecycle rule name
seye3-rule
Status
 Enabled
Scope
Filtered
Prefix
-
Object tags
-
Minimum object size
150 KB (153,600 Bytes)
Maximum object size
2 MB (2,097,152 Bytes)
Review transition and expiration actions
Current version actions
Day 0
Objects uploaded
Day 365
Objects move to Glacier Deep Archive

4. Create a single bucket policy
{
	"Version": "2012-10-17",
	"Statement": [
		{
			"Sid": "Statement1",
			"Principal": {
				"AWS": [
					"arn:aws:iam::403531065616:root"
				]
			},
			"Effect": "Allow",
			"Action": [
				"s3:PutObject"
			],
			"Resource": [
				"arn:aws:s3:::seye3-bucket/*"
			]
		}
	]
}
5. Delete all policies

6. Delete S3 bucket



For guide, kindly visit

https://docs.aws.amazon.com/cli/latest/reference/s3api/create-bucket.html

https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html

https://docs.aws.amazon.com/cli/latest/userguide/cli-services-s3-commands.html
