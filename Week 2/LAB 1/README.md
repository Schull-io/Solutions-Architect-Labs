This task will get you acquainted on how to deploy VPC 


Task 1: Deploy VPC using Management console
1. Launch the AWS Management Console
2. Launch a VPC with one public and one private subnets.
3. Create two route table and associate  each one to each subnets
4. Attach an internet gateway to the VPC and a NAT gateway to the private subnet.
5. Launch a Linux instance into this VPC and attach the subnet
6. Test the network connectivity
7. Perform clean up actions







For guide, you are check the links below:

https://docs.aws.amazon.com/cli/latest/reference/ec2/

https://docs.aws.amazon.com/cli/latest/reference/ec2/describe-vpcs.html





**1. Launch the AWS Management Console**

I launched the Aws management console 

**Launch a VPC with one public and one private subnets.**
I searched the vpc on the search engine and clicked on vpc.


I launched the vpc wizard. 
I created the vpc **vpc-069c687691f4e225b** | project-vpc with public subnet **subnet-099324cf9b2b61957** and private subnet **subnet-07cbf83442c5256ef**


 **Create two route table and associate  each one to each subnets**
 
 the first route table created was **rtb-0a93f65c3a43febd6** asscociated with **subnet-099324cf9b2b61957**
 
 the second route table created was **rtb-00a62d64ac83a0f8c** associated with **subnet-07cbf83442c5256ef**
 
 
 **4. Attach an internet gateway to the VPC and a NAT gateway to the private subnet.**
 the internet gateway 	**igw-0112d38c65e3cce11** has been attached to the **vpc-069c687691f4e225b** and the NAT gateway was successfully created **nat-0c013a6d37b64edd5 / my-nat-gateway-005** to the private subnet **subnet-07cbf83442c5256ef**
 
 
 **5. Launch a Linux instance into this VPC and attach the subnet**
 
 



