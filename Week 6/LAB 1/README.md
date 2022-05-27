# Working with CLoudwatch using AWS Console 

# Monitoring 

1. Enable billing alerts
2. Create a billing alarm
3. Check the alarm status
Details

Name
Billings Alarm

Type
Metric alarm

Description
No description

State
Insufficient data

Threshold
EstimatedCharges >= 10 for 1 datapoints within 6 hours

Last change
2022-05-26 22:57:16

Actions
Actions enabled

Namespace
AWS/Billing

Metric name
EstimatedCharges

Currency
USD

Statistic
Maximum

Period
6 hours

Datapoints to alarm
1 out of 1

Missing data treatment
Treat missing data as missing

Percentiles with low samples
evaluate

ARN
arn:aws:cloudwatch:us-east-1:403531065616:alarm:Billings Alarm

4. Edit a billing alarm
5. Delete a billing alarm


# Alarms

1. Create a CPU usage alarm
Details

Name
CPU Usage

Type
Metric alarm

Description
No description

State
Insufficient data

Threshold
ResourceCount >= 5 for 1 datapoints within 5 minutes

Last change
2022-05-26 23:05:00

Actions
Actions enabled

Namespace
AWS/Usage

Metric name
ResourceCount

Type
Resource

Resource
vCPU

Service
EC2

Class
Standard/OnDemand

Statistic
Average

Period
5 minutes

Datapoints to alarm
1 out of 1

Missing data treatment
Treat missing data as missing

Percentiles with low samples
evaluate

ARN
arn:aws:cloudwatch:us-east-1:403531065616:alarm:CPU Usage

2. Create a load balancer latency alarm that sends email

Details

Name
Balancers

Type
Metric alarm

Description
No description

State
Insufficient data

Threshold
CallCount > the band (width: 2) for 1 datapoints within 5 minutes

Last change
2022-05-26 23:10:34

Actions
Actions enabled

Namespace
AWS/Usage

Metric name
CallCount

Type
API

Resource
DescribeLoadBalancers

Service
Elastic Load Balancing

Class
None
Statistic

Average
Period

5 minutes
Datapoints to alarm

1 out of 1
Missing data treatment

Treat missing data as missing
Percentiles with low samples
evaluate

ARN
arn:aws:cloudwatch:us-east-1:403531065616:alarm:Balancers

3. Create a CloudWatch alarm based on a static threshold

Details

Name
Load Balancer

Type
Metric alarm

Description
No description

State
Insufficient data

Threshold
CallCount > 5 for 1 datapoints within 5 minutes

Last change
2022-05-26 23:07:20

Actions
Actions enabled

Namespace
AWS/Usage

Metric name
CallCount


Type
API

Resource
DescribeLoadBalancers

Service
Elastic Load Balancing

Class
None

Statistic
Average

Period
5 minutes

Datapoints to alarm
1 out of 1
Missing data treatment

Treat missing data as missing
Percentiles with low samples

evaluate

ARN
arn:aws:cloudwatch:us-east-1:403531065616:alarm:Load Balancer


Guide:
https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/gs_monitor_estimated_charges_with_cloudwatch.html

https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html

https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html








