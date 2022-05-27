Working with IAM management console

Tasks

1. Login to your root account
2. Create an IAM group with S3 read only acess (S3 support).
3. Create an IAM group with EC2 read only acess (EC2 support)
4. Create an IAM group with EC2 full access (EC2 admin)
5. Create 3 IAM users and add to the each group above as descibe below:


user      group          permissions
user1     EC2 support     Read-Only access to Amazon EC2
user2     S3 support      Read-Only access to Amazon S3
user3     EC2 admin       Full access to Amazon EC2 instances

Users (3)Info
An IAM user is an identity with long-term credentials that is used to interact with AWS in an account.
DeleteAdd users
Find users by username or access key

1



User name
Groups
Last activity
MFA
Password age
Active key age

User1	
EC2-Support
Never
None
4 minutes ago
-

User2	
S3-Support
Never
None
1 minute ago
-

User3	
EC2-Admin
Never
None
Now
-

6. Test your design

7. Perform clean up operations


Replicate the process above for  Schulltech organization descrcibed below:


user               group                       permissions
adminstaff         EC2 support          Read-Only access to Amazon EC2
Techstaff          S3 support           Full access to S3
ITexpert           EC2/SDK admin        full access to EC2 and SDK
financialmanager     billingcontrol      Billing Full Access  
financeuser          billinguser          Billing view access

Users (5)Info
An IAM user is an identity with long-term credentials that is used to interact with AWS in an account.
DeleteAdd users
Find users by username or access key

1



User name
Groups
Last activity
MFA
Password age
Active key age

AdminStaff	
EC2-Support
Never
None
10 minutes ago
-

FinancialManager	
BillingControl
Never
None
2 minutes ago
-

FinancialUser	
BillingUser
Never
None
Now
-

ITExpert	
EC2-SDK-Admin
Never
None
3 minutes ago
-

TechStaff	
S3-Support
Never
None
6 minutes ago
-

https://docs.aws.amazon.com/IAM/latest/UserGuide/tutorial_users-self-manage-mfa-and-creds.html


