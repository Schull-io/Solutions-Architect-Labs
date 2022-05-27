#  Working with EBS

Tasks:
1. Create an Amazon EBS volume

Details
Volume ID
vol-070e924b928126548
Size
100 GiB
Type
gp2
Volume status
Okay
Volume state
Available
IOPS
300
Throughput
-
Encryption
Not encrypted
KMS key ID
-
KMS key alias
-
KMS key ARN
-
Snapshot
-
Availability Zone
us-east-1a
Created
Fri May 27 2022 02:29:23 GMT+0100 (West Africa Standard Time)
Multi-Attach enabled
No
Attached Instances
-

2. Attach and mount your volume to an EC2 instance
Details
Volume ID
vol-070e924b928126548
Size
100 GiB
Type
gp2
Volume status
Okay
Volume state
In-use
IOPS
300
Throughput
-
Encryption
Not encrypted
KMS key ID
-
KMS key alias
-
KMS key ARN
-
Snapshot
-
Availability Zone
us-east-1a
Created
Fri May 27 2022 02:29:23 GMT+0100 (West Africa Standard Time)
Multi-Attach enabled
No
Attached Instances
i-069e998eb11f42167 (SeyeServer): /dev/sdf (attaching)

3. Create a snapshot of your volume

Snapshot settings
Snapshot ID
snap-0aa85f191ea60cf30
Size
100 GiB
Progress
Available (100%)
Snapshot status
Completed
Owner
403531065616
Volume ID
vol-070e924b928126548
Started
Fri May 27 2022 02:50:41 GMT+0100 (West Africa Standard Time)
Product codes
-
Encryption
Not encrypted
KMS key ID
-
KMS key alias
-
KMS key ARN
-
Fast snapshot restore
-
Description
SeyeEBS-Snapshot

4. Create a new volume from your snapshot
Details
Volume ID
vol-0556395d9c0ed83e5
Size
100 GiB
Type
gp2
Volume status
Okay
Volume state
Available
IOPS
300
Throughput
-
Encryption
Not encrypted
KMS key ID
-
KMS key alias
-
KMS key ARN
-
Snapshot
snap-0aa85f191ea60cf30
Availability Zone
us-east-1a
Created
Fri May 27 2022 02:53:38 GMT+0100 (West Africa Standard Time)
Multi-Attach enabled
No
Attached Instances
-

5. Attach and mount the new volume to your EC2 instance
Details
Volume ID
vol-0556395d9c0ed83e5
Size
100 GiB
Type
gp2
Volume status
Okay
Volume state
In-use
IOPS
300
Throughput
-
Encryption
Not encrypted
KMS key ID
-
KMS key alias
-
KMS key ARN
-
Snapshot
snap-0aa85f191ea60cf30
Availability Zone
us-east-1a
Created
Fri May 27 2022 02:53:38 GMT+0100 (West Africa Standard Time)
Multi-Attach enabled
No
Attached Instances
i-069e998eb11f42167 (SeyeServer): /dev/sdg (attached)


Guide:

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volumes.html

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-attaching-volume.html
