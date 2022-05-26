Creating a User Pool

Tasks: 
1. Go to the Amazon Cognito console. 
2. Choose Manage User Pools.
3. Choose Create a user pool.
4. Enter a name for your user pool and choose Review defaults to save the name.
5. On the Review page, choose Create pool.

MyDevPool
Pool Id us-east-1_zko2CAhS6
Pool ARN arn:aws:cognito-idp:us-east-1:403531065616:userpool/us-east-1_zko2CAhS6
Estimated number of users 0
Required attributes email
Alias attributes none
Username attributes none
Enable case insensitivity? Yes
Custom attributes Choose custom attributes...
Minimum password length 8
Password policy uppercase letters, lowercase letters, special characters, numbers
User sign ups allowed? Users can sign themselves up
FROM email address Default
Email Delivery through Amazon SES No
Note: You have chosen to have Cognito send emails on your behalf. Best practices suggest that customers send emails through Amazon SES for production User Pools due to a daily email limit. Learn more about email best practices.
MFA Enable MFA...
Verifications Email
Advanced security Enable advanced security...
Tags Choose tags for your user pool
App clients Add app client...
Triggers Add triggers...


Guide:

https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-scenarios.html

https://docs.aws.amazon.com/cognito/latest/developerguide/tutorial-create-identity-pool.html