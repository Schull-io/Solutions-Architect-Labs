This task will get you acquainted on how to deploy VPC 


Task 1: Deploy VPC using Management console
1. Launch the AWS Management Console

2. Launch a VPC with one public and one private subnets.
vpc-01dfecf5ee98303fc / seye-vpc

Actions
DetailsInfo
VPC ID
vpc-01dfecf5ee98303fc
Tenancy
Default
Default VPC
No
Route 53 Resolver DNS Firewall rule groups
–
State
 Available
DHCP options set
dopt-02d867fe55784413c
IPv4 CIDR
10.0.0.0/16
Owner ID
403531065616
DNS hostnames
Enabled
Main route table
rtb-00f65870980f382ce
IPv6 pool
–
DNS resolution
Enabled
Main network ACL
acl-0257b977dff0d44a5
IPv6 CIDR (Network border group)
–

a. Private Subnet
Details
Subnet ID
subnet-03484e1e409f1f43d
Available IPv4 addresses
4090
Network border group
us-east-1
Default subnet
No
Customer-owned IPv4 pool
–
IPv6-only
No
DNS64
Disabled
Subnet ARN
arn:aws:ec2:us-east-1:403531065616:subnet/subnet-03484e1e409f1f43d
IPv6 CIDR
–
VPC
vpc-01dfecf5ee98303fc | seye-vpc
Auto-assign public IPv4 address
No
Outpost ID
–
Hostname type
IP name
Owner
403531065616
State
 Available
Availability Zone
us-east-1a
Route table
rtb-034df4d367e50505d | seye-rtb-private1-us-east-1a
Auto-assign IPv6 address
No
IPv4 CIDR reservations
–
Resource name DNS A record
Disabled
IPv4 CIDR
10.0.128.0/20
Availability Zone ID
use1-az6
Network ACL
acl-0257b977dff0d44a5
Auto-assign customer-owned IPv4 address
No
IPv6 CIDR reservations
–
Resource name DNS AAAA record
Disabled


b. Public Subnet
Details
Subnet ID
subnet-03b66303e8ca989bc
Available IPv4 addresses
4091
Network border group
us-east-1
Default subnet
No
Customer-owned IPv4 pool
–
IPv6-only
No
DNS64
Disabled
Subnet ARN
arn:aws:ec2:us-east-1:403531065616:subnet/subnet-03b66303e8ca989bc
IPv6 CIDR
–
VPC
vpc-01dfecf5ee98303fc | seye-vpc
Auto-assign public IPv4 address
No
Outpost ID
–
Hostname type
IP name
Owner
403531065616
State
 Available
Availability Zone
us-east-1a
Route table
rtb-061710887134fe059 | seye-rtb-public
Auto-assign IPv6 address
No
IPv4 CIDR reservations
–
Resource name DNS A record
Disabled
IPv4 CIDR
10.0.0.0/20
Availability Zone ID
use1-az6
Network ACL
acl-0257b977dff0d44a5
Auto-assign customer-owned IPv4 address
No
IPv6 CIDR reservations
–
Resource name DNS AAAA record
Disabled

3. Create two route table and associate  each one to each subnets
Route table ID
rtb-061710887134fe059
VPC
vpc-01dfecf5ee98303fc | seye-vpc
Main
No
Owner ID
403531065616
Explicit subnet associations
subnet-03b66303e8ca989bc / seye-subnet-public1-us-east-1a
Edge associations
–

Route table ID
rtb-034df4d367e50505d
VPC
vpc-01dfecf5ee98303fc | seye-vpc
Main
No
Owner ID
403531065616
Explicit subnet associations
subnet-03484e1e409f1f43d / seye-subnet-private1-us-east-1a
Edge associations
–
4. Attach an internet gateway to the VPC and a NAT gateway to the private subnet
NAT Gateway
NAT gateway ID
nat-01be5fef041cd36a2
NAT gateway ARN
arn:aws:ec2:us-east-1:403531065616:natgateway/nat-01be5fef041cd36a2
VPC
vpc-01dfecf5ee98303fc / seye-vpc
Connectivity type
Public
Elastic IP address
34.199.87.52
Subnet
subnet-03484e1e409f1f43d / seye-subnet-private1-us-east-1a
State
 Available
Private IP address
10.0.128.193
Created
Thursday, May 26, 2022, 18:57:57 GMT+1
State message
–
Network interface ID
eni-0c2b5cfb58d431714  
Deleted
–

Internet Gateway
Details
Internet gateway ID
igw-06f389aeef30519f4
State
 Attached
VPC ID
vpc-01dfecf5ee98303fc | seye-vpc
Owner
403531065616

5. Lauch a Linux instance into this VPC and attach the subnet
Instance ID
 i-099cfe75066b07df4 (seye-server)
Public IPv4 address
–
Private IPv4 addresses
 10.0.142.22
IPv6 address
–
Instance state
 Running
Public IPv4 DNS
–
Hostname type
IP name: ip-10-0-142-22.ec2.internal
Private IP DNS name (IPv4 only)
 ip-10-0-142-22.ec2.internal
Answer private resource DNS name
IPv4 (A)
Instance type
t2.micro
Elastic IP addresses
–
Auto-assigned IP address
–
VPC ID
 vpc-01dfecf5ee98303fc (seye-vpc) 
AWS Compute Optimizer finding
Opt-in to AWS Compute Optimizer for recommendations. | Learn more 
IAM Role
–
Subnet ID
 subnet-03484e1e409f1f43d (seye-subnet-private1-us-east-1a) 
6. Test the network connectivity
7. Perform clean up actions
Done






For guide, you are check the links below:

https://docs.aws.amazon.com/cli/latest/reference/ec2/

https://docs.aws.amazon.com/cli/latest/reference/ec2/describe-vpcs.html

