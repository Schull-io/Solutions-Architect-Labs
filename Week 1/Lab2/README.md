# Task 2: Create S3 bucket with bucket policies and life cycle management

1. Launch AWS Console
2. Create a S3 bucket with enforced ownership
3. Create a single lifecycle policy
4. Create a single bucket policy
5. Delete all policies
6. Delete S3 bucket



# ANSWRES TO WEEK 1 TASK 2 LAB
# (TASK: Create S3 bucket with bucket policies and life cycle management)

1. LAUNCHING AWS CONSOLE
I launched my AWS CLOUDSHELL from my AWS MANAGEMENT CONSOLE by clicking pn the AWS CLOUDSHELL icon at the top right corner of the console, which opened up the command line interface for me to type my commands and continue interacting with aws.

2. Create a S3 bucket with enforced ownership.
To create a bucket with owner enforced setting I used the following command:

aws s3api create-bucket \
    --bucket enforced-demo \
    --region us-east-1 \
    --object-ownership BucketOwnerEnforced

3.  Create a single lifecycle policy
To create a single lyfecycle policy, I used the following command:

aws s3api put-bucket-lifecycle
 --bucket enforced-demo
  --lifecycle-configuration file://lifecycle.json

For guide, kindly visit

https://docs.aws.amazon.com/cli/latest/reference/s3api/create-bucket.html

https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html

https://docs.aws.amazon.com/cli/latest/userguide/cli-services-s3-commands.html
