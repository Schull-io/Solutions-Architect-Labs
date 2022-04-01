This Week lab will focus on getting you acquainted with S3 using the aws cli

# Task 1: Create a S3 bucket using AWS CLI

1. Lauch AWS cloud shell
2. Create a S3 bucket 
3. Create a folder in your S3 bucket
4. Upload objects to your S3 bucket
5. List the object in your S3 bucket
6. Download Object from your S3 bucket
7. Delete object in your s3 bucket
8. Delete your S3 bucket

# ANSWERS TO WEEK 1 LAB 1  
# (Task 1: Create a S3 bucket using AWS CLI)
1. LAUNCH AWS CLOUD SHELL
I launched my AWS CLOUDSHELL from my AWS MANAGEMENT CONSOLE by clicking pn the AWS CLOUDSHELL icon at the top right corner of the console, which opened up the command line interface for me to type my commands and continue interacting with aws.

2. CREATE AN S3 BUCKET USING CLI
I used the below command lines to create a bucket which I manes Harry-demo-bucket, I also specified the region.

aws s3api create-bucket \
    --bucket Harry-demo-bucket \
    --region us-east-1

3. CREATING A FOLDER INSIDE MY S3 BUCKET USING CLI

I created a folder called text-folder inside my S3 bucket with the command below:
aws s3api put-object
 --bucket Harry-demo-bucket \
 --key text-folder/  

4. UPLOAD OBJECTS IN YOUR S3 BUCKET USING CLI
To upload an object to my s3 bucket, I used the following command:

aws s3api put-object 
--bucket text-content 
--key dir-1/my_images.tar.bz2 
--body my_images.tar.bz2

5. LIST THE OBJECTS IN MY S3 BUCKET
To list the objects in my s3 bucket, I used the following commands:

aws s3api list-objects 
--bucket text-content
--query 'Contents[].{Key: Key, Size: Size}'

6. DOWNLOAD OBJECTS FROM MY S3 BUCKET
To download objects, I used the following commands:

aws s3 cp s3://Harry-demo-bucket/demo-file.txt ./destination

7. DELETE OBJECT IN MY S3 BUCKET.
To delete an object in my s3 bucket I simply used the following command:

aws s3api delete-object 
--bucket Harry-demo-bucket 
--key demo-file.txt

8. DELETE YOUR S3 BUCKET
To delete my s3 bucket I simply used the following command:

aws s3api delete-bucket 
--bucketHarry-demo-bucket  
--region us-east-1






For guide, kindly visit

https://docs.aws.amazon.com/cli/latest/reference/s3api/create-bucket.html

https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html

https://docs.aws.amazon.com/cli/latest/userguide/cli-services-s3-commands.html
