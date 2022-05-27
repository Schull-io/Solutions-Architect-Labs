# Working with EC2 instance using the AWS CLI / Programmable access

Tasks:

1. Using your default vpc, find the public subnet

VPC ID
vpc-0e2340d1b645e39be
Tenancy
Default
Default VPC
Yes
Route 53 Resolver DNS Firewall rule groups
–
State
 Available
DHCP options set
dopt-02d867fe55784413c
IPv4 CIDR
172.31.0.0/16
Owner ID
403531065616
DNS hostnames
Enabled
Main route table
rtb-02178a61d3c140d19
IPv6 pool
–
DNS resolution
Enabled
Main network ACL
acl-05d166ff08609f173
IPv6 CIDR (Network border group)
–

2. Create a security group

3. Launch an instance with a web server with termination protection enabled
Instance ID
 i-0703f8a25191f5cf5 (NewServer)
Public IPv4 address
 54.82.116.134 | open address 
Private IPv4 addresses
 172.31.20.27
IPv6 address
–
Instance state
 Running
Public IPv4 DNS
 ec2-54-82-116-134.compute-1.amazonaws.com | open address 
Hostname type
IP name: ip-172-31-20-27.ec2.internal
Private IP DNS name (IPv4 only)
 ip-172-31-20-27.ec2.internal
Answer private resource DNS name
IPv4 (A)
Instance type
t2.micro
Elastic IP addresses
–
Auto-assigned IP address
 54.82.116.134 [Public IP]
VPC ID
 vpc-0e2340d1b645e39be 
AWS Compute Optimizer finding
Opt-in to AWS Compute Optimizer for recommendations. | Learn more 
IAM Role
–
Subnet ID
 subnet-09e8a68150e696e76 
Auto Scaling Group name

Platform
 Amazon Linux (Inferred)
AMI ID
 ami-0022f774911c1d690
Monitoring
disabled
Platform details
 Linux/UNIX
AMI name
 amzn2-ami-kernel-5.10-hvm-2.0.20220426.0-x86_64-gp2
Termination protection
Enabled

4. Monitor Your EC2 instance; view the types of metrics that are collected for an EC2 instance

5. Modify the security group that your web server is using to allow HTTP access
Instance ID
 i-0703f8a25191f5cf5 (NewServer)
Public IPv4 address
 54.82.116.134 | open address 
Private IPv4 addresses
 172.31.20.27
IPv6 address
–
Instance state
 Running
Public IPv4 DNS
 ec2-54-82-116-134.compute-1.amazonaws.com | open address 
Hostname type
IP name: ip-172-31-20-27.ec2.internal
Private IP DNS name (IPv4 only)
 ip-172-31-20-27.ec2.internal
Answer private resource DNS name
IPv4 (A)
Instance type
t2.micro
Elastic IP addresses
–
Auto-assigned IP address
 54.82.116.134 [Public IP]
VPC ID
 vpc-0e2340d1b645e39be 
AWS Compute Optimizer finding
Opt-in to AWS Compute Optimizer for recommendations. | Learn more 
IAM Role
–
6. Resize your Amazon EC2 instance to scale


Guide
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/terminating-instances.html


https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-resize.html