This Week lab will focus on getting you acquainted with Amazon S3 using the aws cli

# Task 1: Create a S3 bucket using AWS CLI

1. Lauch AWS cloud shell
2. Create a S3 bucket 
[cloudshell-user@ip-10-1-155-161 ~]$ aws s3api create-bucket \
>     --bucket seye2-bucket \
>     --region us-east-1
{
    "Location": "/seye2-bucket"
}
[cloudshell-user@ip-10-1-155-161 ~]$ 

3. Create a folder in your S3 bucket
4. Upload objects to your S3 bucket
5. List the object in your S3 bucket
[cloudshell-user@ip-10-0-145-53 ~]$ aws s3api list-objects --bucket seye2-bucket --prefix "docs/"
{
    "Contents": [
        {
            "Key": "docs/",
            "LastModified": "2022-05-27T00:32:49+00:00",
            "ETag": "\"d41d8cd98f00b204e9800998ecf8427e\"",
            "Size": 0,
            "StorageClass": "STANDARD",
            "Owner": {
                "DisplayName": "seyeonigbinde87",
                "ID": "017e4966f32aad4346cbc465995222dd6e2c82fef495042f72fe474d10f2b8cd"
            }
        },
        {
            "Key": "docs/cacer-icon.png",
            "LastModified": "2022-05-27T01:24:08+00:00",
            "ETag": "\"aed7eff789d055e6806f92bdb6b22786\"",
            "Size": 120508,
            "StorageClass": "STANDARD",
            "Owner": {
                "DisplayName": "seyeonigbinde87",
                "ID": "017e4966f32aad4346cbc465995222dd6e2c82fef495042f72fe474d10f2b8cd"
            }
        },
        {
            "Key": "docs/cacer-icon2.png",
            "LastModified": "2022-05-27T01:24:07+00:00",
            "ETag": "\"5e6494e0f46b1dfae0fb4e644a4f3d63\"",
            "Size": 126189,
            "StorageClass": "STANDARD",
            "Owner": {
                "DisplayName": "seyeonigbinde87",
                "ID": "017e4966f32aad4346cbc465995222dd6e2c82fef495042f72fe474d10f2b8cd"
            }
        }
    ]
}
6. Download Object from your S3 bucket
7. Delete object in your s3 bucket
8. Delete your S3 bucket





For guide, kindly visit

https://docs.aws.amazon.com/cli/latest/reference/s3api/create-bucket.html

https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html

https://docs.aws.amazon.com/cli/latest/userguide/cli-services-s3-commands.html
