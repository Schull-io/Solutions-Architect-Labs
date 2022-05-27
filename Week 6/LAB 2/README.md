#  Working with AWS Cloudtrail

1. Review AWS account activity in event history
Event history (8)Info


Download events
Create Athena table
Event history shows you the last 90 days of management events.
We can't find a match.
false
30m
1h
3h
12h
Clear
Custom

1



Event name
Event time
User name
Event source
Resource type
Resource name

Event name
Event time
User name
Event source
Resource type
Resource name

DeleteAlarms	May 27, 2022, 00:16:13 (UTC+01:00)	root	monitoring.amazonaws.com
AWS::CloudWatch::Alarm, AWS::CloudWatch::Alarm, AWS::CloudWatch::Alarm	Balancers, CPU Usage, Load Balancer

PutMetricAlarm	May 27, 2022, 00:10:35 (UTC+01:00)	root	monitoring.amazonaws.com
AWS::CloudWatch::Alarm	Balancers

PutMetricAlarm	May 27, 2022, 00:07:20 (UTC+01:00)	root	monitoring.amazonaws.com
AWS::CloudWatch::Alarm	Load Balancer

PutMetricAlarm	May 27, 2022, 00:05:00 (UTC+01:00)	root	monitoring.amazonaws.com
AWS::CloudWatch::Alarm	CPU Usage

DeleteAlarms	May 26, 2022, 23:59:54 (UTC+01:00)	root	monitoring.amazonaws.com
AWS::CloudWatch::Alarm	Billings Alarm

DeleteAlarms	May 26, 2022, 23:59:31 (UTC+01:00)	root	monitoring.amazonaws.com
AWS::CloudWatch::Alarm	Billing Alarm

PutMetricAlarm	May 26, 2022, 23:57:16 (UTC+01:00)	root	monitoring.amazonaws.com
AWS::CloudWatch::Alarm	Billings Alarm

PutMetricAlarm	May 26, 2022, 23:54:47 (UTC+01:00)	root	monitoring.amazonaws.com
AWS::CloudWatch::Alarm	Billing Alarm

2. Create your first trail

General details

Trail logging
 Logging

Trail name
EventTrails

Multi-region trail
Yes

Apply trail to my organization
Not enabled

Trail log location
aws-cloudtrail-logs-403531065616-a696ca0b/AWSLogs/403531065616

Last log file delivered
-

Log file SSE-KMS encryption
Enabled

AWS KMS key
arn:aws:kms:us-east-1:403531065616:key/ed769a89-7d98-496e-ab14-2622dfb0c004

AWS KMS key alias
myEventTrail

Log file validation
Enabled

Last file validation delivered
-
SNS notification delivery
Disabled
Last SNS notification
-

3. View your log files



Guide:
https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-tutorial.html
