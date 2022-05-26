Task :  Create a dual Stack VPC and subnets using AWS CLI

Step:
1. Launch a non-default VPC
{
    "Vpc": {
        "CidrBlock": "10.0.0.0/16",
        "DhcpOptionsId": "dopt-02d867fe55784413c",
        "State": "pending",
        "VpcId": "vpc-0e7d4bded747cf80e",
        "OwnerId": "403531065616",
        "InstanceTenancy": "default",
        "Ipv6CidrBlockAssociationSet": [
            {
                "AssociationId": "vpc-cidr-assoc-01c949f55b2d955c7",
                "Ipv6CidrBlock": "",
                "Ipv6CidrBlockState": {
                    "State": "associating"
                },
                "NetworkBorderGroup": "us-east-1",
                "Ipv6Pool": "Amazon"
            }
        ],
        "CidrBlockAssociationSet": [
            {
                "AssociationId": "vpc-cidr-assoc-0ea3b1c7439ed4087",
                "CidrBlock": "10.0.0.0/16",
                "CidrBlockState": {
                    "State": "associated"
                }
            }
        ],
        "IsDefault": false
    }
}
{
    "Vpcs": [
        {
            "CidrBlock": "10.0.0.0/16",
            "DhcpOptionsId": "dopt-02d867fe55784413c",
            "State": "available",
            "VpcId": "vpc-0e7d4bded747cf80e",
            "OwnerId": "403531065616",
            "InstanceTenancy": "default",
            "Ipv6CidrBlockAssociationSet": [
                {
                    "AssociationId": "vpc-cidr-assoc-01c949f55b2d955c7",
                    "Ipv6CidrBlock": "2600:1f18:984:b600::/56",
                    "Ipv6CidrBlockState": {
                        "State": "associated"
                    },
                    "NetworkBorderGroup": "us-east-1",
                    "Ipv6Pool": "Amazon"
                }
            ],
            "CidrBlockAssociationSet": [
                {
                    "AssociationId": "vpc-cidr-assoc-0ea3b1c7439ed4087",
                    "CidrBlock": "10.0.0.0/16",
                    "CidrBlockState": {
                        "State": "associated"
                    }
                }
            ],
            "IsDefault": false
        }
    ]
}
2. Create two subnets 
{
    "Subnet": {
        "AvailabilityZone": "us-east-1d",
        "AvailabilityZoneId": "use1-az4",
        "AvailableIpAddressCount": 251,
        "CidrBlock": "10.0.0.0/24",
        "DefaultForAz": false,
        "MapPublicIpOnLaunch": false,
        "State": "available",
        "SubnetId": "subnet-07e793d033c1e032c",
        "VpcId": "vpc-0e7d4bded747cf80e",
        "OwnerId": "403531065616",
        "AssignIpv6AddressOnCreation": false,
        "Ipv6CidrBlockAssociationSet": [
            {
                "AssociationId": "subnet-cidr-assoc-07e951abfc9864242",
                "Ipv6CidrBlock": "2600:1f18:984:b600::/64",
                "Ipv6CidrBlockState": {
                    "State": "associating"
                }
            }
        ],
        "SubnetArn": "arn:aws:ec2:us-east-1:403531065616:subnet/subnet-07e793d033c1e032c",
        "EnableDns64": false,
        "Ipv6Native": false,
        "PrivateDnsNameOptionsOnLaunch": {
            "HostnameType": "ip-name",
            "EnableResourceNameDnsARecord": false,
            "EnableResourceNameDnsAAAARecord": false
        }
    }
}

{
    "Subnet": {
        "AvailabilityZone": "us-east-1d",
        "AvailabilityZoneId": "use1-az4",
        "AvailableIpAddressCount": 251,
        "CidrBlock": "10.0.1.0/24",
        "DefaultForAz": false,
        "MapPublicIpOnLaunch": false,
        "State": "available",
        "SubnetId": "subnet-060b6b0577b7b4fe7",
        "VpcId": "vpc-0e7d4bded747cf80e",
        "OwnerId": "403531065616",
        "AssignIpv6AddressOnCreation": false,
        "Ipv6CidrBlockAssociationSet": [
            {
                "AssociationId": "subnet-cidr-assoc-05f4c0bc4012406fa",
                "Ipv6CidrBlock": "2600:1f18:984:b601::/64",
                "Ipv6CidrBlockState": {
                    "State": "associating"
                }
            }
        ],
        "SubnetArn": "arn:aws:ec2:us-east-1:403531065616:subnet/subnet-060b6b0577b7b4fe7",
        "EnableDns64": false,
        "Ipv6Native": false,
        "PrivateDnsNameOptionsOnLaunch": {
            "HostnameType": "ip-name",
            "EnableResourceNameDnsARecord": false,
            "EnableResourceNameDnsAAAARecord": false
        }
    }
}

3. Create an internet gateway to one of the subnets with route table 
{
    "InternetGateway": {
        "Attachments": [],
        "InternetGatewayId": "igw-00e0562a46de6be72",
        "OwnerId": "403531065616",
        "Tags": []
    }
}
{
    "RouteTable": {
        "Associations": [],
        "PropagatingVgws": [],
        "RouteTableId": "rtb-05b0c900a380bca8e",
        "Routes": [
            {
                "DestinationCidrBlock": "10.0.0.0/16",
                "GatewayId": "local",
                "Origin": "CreateRouteTable",
                "State": "active"
            },
            {
                "DestinationIpv6CidrBlock": "2600:1f18:984:b600::/56",
                "GatewayId": "local",
                "Origin": "CreateRouteTable",
                "State": "active"
            }
        ],
        "Tags": [],
        "VpcId": "vpc-0e7d4bded747cf80e",
        "OwnerId": "403531065616"
    }
}
{
    "RouteTables": [
        {
            "Associations": [],
            "PropagatingVgws": [],
            "RouteTableId": "rtb-05b0c900a380bca8e",
            "Routes": [
                {
                    "DestinationCidrBlock": "10.0.0.0/16",
                    "GatewayId": "local",
                    "Origin": "CreateRouteTable",
                    "State": "active"
                },
                {
                    "DestinationIpv6CidrBlock": "2600:1f18:984:b600::/56",
                    "GatewayId": "local",
                    "Origin": "CreateRouteTable",
                    "State": "active"
                },
                {
                    "DestinationIpv6CidrBlock": "::/0",
                    "GatewayId": "igw-00e0562a46de6be72",
                    "Origin": "CreateRoute",
                    "State": "active"
                }
            ],
            "Tags": [],
            "VpcId": "vpc-0e7d4bded747cf80e",
            "OwnerId": "403531065616"
        }
    ]
}
[
    {
        "ID": "subnet-07e793d033c1e032c",
        "IPv4CIDR": "10.0.0.0/24",
        "IPv6CIDR": [
            "2600:1f18:984:b600::/64"
        ]
    },
    {
        "ID": "subnet-060b6b0577b7b4fe7",
        "IPv4CIDR": "10.0.1.0/24",
        "IPv6CIDR": [
            "2600:1f18:984:b601::/64"
        ]
    }
]

{
    "AssociationId": "rtbassoc-04c71c64c572f9d7d",
    "AssociationState": {
        "State": "associated"
    }
}
4. Configure an egress-only private subnet
{
    "EgressOnlyInternetGateway": {
        "Attachments": [
            {
                "State": "attached",
                "VpcId": "vpc-0e7d4bded747cf80e"
            }
        ],
        "EgressOnlyInternetGatewayId": "eigw-064fb09ff8a80e3a0"
    }
}
{
    "RouteTable": {
        "Associations": [],
        "PropagatingVgws": [],
        "RouteTableId": "rtb-0a0b806b1fb814352",
        "Routes": [
            {
                "DestinationCidrBlock": "10.0.0.0/16",
                "GatewayId": "local",
                "Origin": "CreateRouteTable",
                "State": "active"
            },
            {
                "DestinationIpv6CidrBlock": "2600:1f18:984:b600::/56",
                "GatewayId": "local",
                "Origin": "CreateRouteTable",
                "State": "active"
            }
        ],
        "Tags": [],
        "VpcId": "vpc-0e7d4bded747cf80e",
        "OwnerId": "403531065616"
    }
}
{
    "AssociationId": "rtbassoc-096dc40155e1e5711",
    "AssociationState": {
        "State": "associated"
    }
}
5. Modify the IPv6 addressing behavior of the subnets
6. Lauch an instance into your public subnet
{
    "GroupId": "sg-04bf1284df702c5e3"
}
{
    "Return": true,
    "SecurityGroupRules": [
        {
            "SecurityGroupRuleId": "sgr-0c7ecec6d67e4217e",
            "GroupId": "sg-04bf1284df702c5e3",
            "GroupOwnerId": "403531065616",
            "IsEgress": false,
            "IpProtocol": "tcp",
            "FromPort": 22,
            "ToPort": 22,
            "CidrIpv6": "::/0"
        }
    ]
}
{
    "Groups": [],
    "Instances": [
        {
            "AmiLaunchIndex": 0,
            "ImageId": "ami-0de53d8956e8dcf80",
            "InstanceId": "i-0cea696be7454433e",
            "InstanceType": "t2.micro",
            "KeyName": "SeyeKeyPair",
            "LaunchTime": "2022-05-26T20:55:18+00:00",
            "Monitoring": {
                "State": "disabled"
            },
            "Placement": {
                "AvailabilityZone": "us-east-1d",
                "GroupName": "",
                "Tenancy": "default"
            },
            "PrivateDnsName": "ip-10-0-0-135.ec2.internal",
            "PrivateIpAddress": "10.0.0.135",
            "ProductCodes": [],
            "PublicDnsName": "",
            "State": {
                "Code": 0,
                "Name": "pending"
            },
            "StateTransitionReason": "",
            "SubnetId": "subnet-07e793d033c1e032c",
            "VpcId": "vpc-0e7d4bded747cf80e",
            "Architecture": "x86_64",
            "BlockDeviceMappings": [],
            "ClientToken": "b7852ab1-8bec-45e3-8659-979608ffba0b",
            "EbsOptimized": false,
            "EnaSupport": true,
            "Hypervisor": "xen",
            "NetworkInterfaces": [
                {
                    "Attachment": {
                        "AttachTime": "2022-05-26T20:55:18+00:00",
                        "AttachmentId": "eni-attach-055617fba3feb0505",
                        "DeleteOnTermination": true,
                        "DeviceIndex": 0,
                        "Status": "attaching",
                        "NetworkCardIndex": 0
                    },
                    "Description": "",
                    "Groups": [
                        {
                            "GroupName": "SSHAccess",
                            "GroupId": "sg-04bf1284df702c5e3"
                        }
                    ],
                    "Ipv6Addresses": [
                        {
                            "Ipv6Address": "2600:1f18:984:b600:8298:3287:fc85:d472"
                        }
                    ],
                    "MacAddress": "0a:2e:03:1a:2e:f5",
                    "NetworkInterfaceId": "eni-0c44ad4200f52eeb6",
                    "OwnerId": "403531065616",
                    "PrivateIpAddress": "10.0.0.135",
                    "PrivateIpAddresses": [
                        {
                            "Primary": true,
                            "PrivateIpAddress": "10.0.0.135"
                        }
                    ],
                    "SourceDestCheck": true,
                    "Status": "in-use",
                    "SubnetId": "subnet-07e793d033c1e032c",
                    "VpcId": "vpc-0e7d4bded747cf80e",
                    "InterfaceType": "interface"
                }
            ],
            "RootDeviceName": "/dev/xvda",
            "RootDeviceType": "ebs",
            "SecurityGroups": [
                {
                    "GroupName": "SSHAccess",
                    "GroupId": "sg-04bf1284df702c5e3"
                }
            ],
            "SourceDestCheck": true,
            "StateReason": {
                "Code": "pending",
                "Message": "pending"
            },
            "VirtualizationType": "hvm",
            "CpuOptions": {
                "CoreCount": 1,
                "ThreadsPerCore": 1
            },
            "CapacityReservationSpecification": {
                "CapacityReservationPreference": "open"
            },
            "MetadataOptions": {
                "State": "pending",
                "HttpTokens": "optional",
                "HttpPutResponseHopLimit": 1,
                "HttpEndpoint": "enabled",
                "HttpProtocolIpv6": "disabled",
                "InstanceMetadataTags": "disabled"
            },
            "EnclaveOptions": {
                "Enabled": false
            },
            "PrivateDnsNameOptions": {
                "HostnameType": "ip-name",
                "EnableResourceNameDnsARecord": false,
                "EnableResourceNameDnsAAAARecord": false
            },
            "MaintenanceOptions": {
                "AutoRecovery": "default"
            }
        }
    ],
    "OwnerId": "403531065616",
    "ReservationId": "r-0018a52192b64cd20"
}
{
    "Reservations": [
        {
            "Groups": [],
            "Instances": [
                {
                    "AmiLaunchIndex": 0,
                    "ImageId": "ami-0de53d8956e8dcf80",
                    "InstanceId": "i-0cea696be7454433e",
                    "InstanceType": "t2.micro",
                    "KeyName": "SeyeKeyPair",
                    "LaunchTime": "2022-05-26T20:55:18+00:00",
                    "Monitoring": {
                        "State": "disabled"
                    },
                    "Placement": {
                        "AvailabilityZone": "us-east-1d",
                        "GroupName": "",
                        "Tenancy": "default"
                    },
                    "PrivateDnsName": "ip-10-0-0-135.ec2.internal",
                    "PrivateIpAddress": "10.0.0.135",
                    "ProductCodes": [],
                    "PublicDnsName": "",
                    "State": {
                        "Code": 16,
                        "Name": "running"
                    },
                    "StateTransitionReason": "",
                    "SubnetId": "subnet-07e793d033c1e032c",
                    "VpcId": "vpc-0e7d4bded747cf80e",
                    "Architecture": "x86_64",
                    "BlockDeviceMappings": [
                        {
                            "DeviceName": "/dev/xvda",
                            "Ebs": {
                                "AttachTime": "2022-05-26T20:55:19+00:00",
                                "DeleteOnTermination": true,
                                "Status": "attached",
                                "VolumeId": "vol-0d4054fef3fcf4c07"
                            }
                        }
                    ],
                    "ClientToken": "b7852ab1-8bec-45e3-8659-979608ffba0b",
                    "EbsOptimized": false,
                    "EnaSupport": true,
                    "Hypervisor": "xen",
                    "NetworkInterfaces": [
                        {
                            "Attachment": {
                                "AttachTime": "2022-05-26T20:55:18+00:00",
                                "AttachmentId": "eni-attach-055617fba3feb0505",
                                "DeleteOnTermination": true,
                                "DeviceIndex": 0,
                                "Status": "attached",
                                "NetworkCardIndex": 0
                            },
                            "Description": "",
                            "Groups": [
                                {
                                    "GroupName": "SSHAccess",
                                    "GroupId": "sg-04bf1284df702c5e3"
                                }
                            ],
                            "Ipv6Addresses": [
                                {
                                    "Ipv6Address": "2600:1f18:984:b600:8298:3287:fc85:d472"
                                }
                            ],
                            "MacAddress": "0a:2e:03:1a:2e:f5",
                            "NetworkInterfaceId": "eni-0c44ad4200f52eeb6",
                            "OwnerId": "403531065616",
                            "PrivateIpAddress": "10.0.0.135",
                            "PrivateIpAddresses": [
                                {
                                    "Primary": true,
                                    "PrivateIpAddress": "10.0.0.135"
                                }
                            ],
                            "SourceDestCheck": true,
                            "Status": "in-use",
                            "SubnetId": "subnet-07e793d033c1e032c",
                            "VpcId": "vpc-0e7d4bded747cf80e",
                            "InterfaceType": "interface"
                        }
                    ],
                    "RootDeviceName": "/dev/xvda",
                    "RootDeviceType": "ebs",
                    "SecurityGroups": [
                        {
                            "GroupName": "SSHAccess",
                            "GroupId": "sg-04bf1284df702c5e3"
                        }
                    ],
                    "SourceDestCheck": true,
                    "VirtualizationType": "hvm",
                    "CpuOptions": {
                        "CoreCount": 1,
                        "ThreadsPerCore": 1
                    },
                    "CapacityReservationSpecification": {
                        "CapacityReservationPreference": "open"
                    },
                    "HibernationOptions": {
                        "Configured": false
                    },
                    "MetadataOptions": {
                        "State": "applied",
                        "HttpTokens": "optional",
                        "HttpPutResponseHopLimit": 1,
                        "HttpEndpoint": "enabled",
                        "HttpProtocolIpv6": "disabled",
                        "InstanceMetadataTags": "disabled"
                    },
                    "EnclaveOptions": {
                        "Enabled": false
                    },
                    "PlatformDetails": "Linux/UNIX",
                    "UsageOperation": "RunInstances",
                    "UsageOperationUpdateTime": "2022-05-26T20:55:18+00:00",
                    "PrivateDnsNameOptions": {
                        "HostnameType": "ip-name",
                        "EnableResourceNameDnsARecord": false,
                        "EnableResourceNameDnsAAAARecord": false
                    },
                    "Ipv6Address": "2600:1f18:984:b600:8298:3287:fc85:d472",
                    "MaintenanceOptions": {
                        "AutoRecovery": "default"
                    }
                }
            ],
            "OwnerId": "403531065616",
            "ReservationId": "r-0018a52192b64cd20"
        }
    ]
}
7. Launch an instance into your private subnet
{
    "GroupId": "sg-0389502def6d372c0"
}
{
    "Return": true,
    "SecurityGroupRules": [
        {
            "SecurityGroupRuleId": "sgr-0423321823dea2c87",
            "GroupId": "sg-0389502def6d372c0",
            "GroupOwnerId": "403531065616",
            "IsEgress": false,
            "IpProtocol": "tcp",
            "FromPort": 22,
            "ToPort": 22,
            "CidrIpv6": "2600:1f18:984:b600::123/128"
        }
    ]
}
{
    "Return": true,
    "SecurityGroupRules": [
        {
            "SecurityGroupRuleId": "sgr-08ef9d3491a7aeb84",
            "GroupId": "sg-0389502def6d372c0",
            "GroupOwnerId": "403531065616",
            "IsEgress": false,
            "IpProtocol": "icmpv6",
            "FromPort": -1,
            "ToPort": -1,
            "CidrIpv6": "::/0"
        }
    ]
}
{
    "Groups": [],
    "Instances": [
        {
            "AmiLaunchIndex": 0,
            "ImageId": "ami-a4827dc9",
            "InstanceId": "i-0552e16926117b460",
            "InstanceType": "t2.micro",
            "KeyName": "SeyeKeyPair",
            "LaunchTime": "2022-05-26T21:10:19+00:00",
            "Monitoring": {
                "State": "disabled"
            },
            "Placement": {
                "AvailabilityZone": "us-east-1d",
                "GroupName": "",
                "Tenancy": "default"
            },
            "PrivateDnsName": "ip-10-0-1-9.ec2.internal",
            "PrivateIpAddress": "10.0.1.9",
            "ProductCodes": [],
            "PublicDnsName": "",
            "State": {
                "Code": 0,
                "Name": "pending"
            },
            "StateTransitionReason": "",
            "SubnetId": "subnet-060b6b0577b7b4fe7",
            "VpcId": "vpc-0e7d4bded747cf80e",
            "Architecture": "x86_64",
            "BlockDeviceMappings": [],
            "ClientToken": "de80c650-f3d0-45a1-8f84-3a1e91222b8f",
            "EbsOptimized": false,
            "Hypervisor": "xen",
            "NetworkInterfaces": [
                {
                    "Attachment": {
                        "AttachTime": "2022-05-26T21:10:19+00:00",
                        "AttachmentId": "eni-attach-00ee78e65a8c8cda1",
                        "DeleteOnTermination": true,
                        "DeviceIndex": 0,
                        "Status": "attaching",
                        "NetworkCardIndex": 0
                    },
                    "Description": "",
                    "Groups": [
                        {
                            "GroupName": "SSHAccessRestricted",
                            "GroupId": "sg-0389502def6d372c0"
                        }
                    ],
                    "Ipv6Addresses": [
                        {
                            "Ipv6Address": "2600:1f18:984:b601:6979:8479:9152:ff18"
                        }
                    ],
                    "MacAddress": "0a:4c:ea:5b:e4:2f",
                    "NetworkInterfaceId": "eni-0d10e76bc7cb92612",
                    "OwnerId": "403531065616",
                    "PrivateIpAddress": "10.0.1.9",
                    "PrivateIpAddresses": [
                        {
                            "Primary": true,
                            "PrivateIpAddress": "10.0.1.9"
                        }
                    ],
                    "SourceDestCheck": true,
                    "Status": "in-use",
                    "SubnetId": "subnet-060b6b0577b7b4fe7",
                    "VpcId": "vpc-0e7d4bded747cf80e",
                    "InterfaceType": "interface"
                }
            ],
            "RootDeviceName": "/dev/xvda",
            "RootDeviceType": "ebs",
            "SecurityGroups": [
                {
                    "GroupName": "SSHAccessRestricted",
                    "GroupId": "sg-0389502def6d372c0"
                }
            ],
            "SourceDestCheck": true,
            "StateReason": {
                "Code": "pending",
                "Message": "pending"
            },
            "VirtualizationType": "hvm",
            "CpuOptions": {
                "CoreCount": 1,
                "ThreadsPerCore": 1
            },
            "CapacityReservationSpecification": {
                "CapacityReservationPreference": "open"
            },
            "MetadataOptions": {
                "State": "pending",
                "HttpTokens": "optional",
                "HttpPutResponseHopLimit": 1,
                "HttpEndpoint": "enabled",
                "HttpProtocolIpv6": "disabled",
                "InstanceMetadataTags": "disabled"
            },
            "EnclaveOptions": {
                "Enabled": false
            },
            "PrivateDnsNameOptions": {
                "HostnameType": "ip-name",
                "EnableResourceNameDnsARecord": false,
                "EnableResourceNameDnsAAAARecord": false
            },
            "MaintenanceOptions": {
                "AutoRecovery": "default"
            }
        }
    ],
    "OwnerId": "403531065616",
    "ReservationId": "r-0b036d042727be916"
}
8. Perform clean up operations. 


https://docs.aws.amazon.com/vpc/latest/userguide/vpc-subnets-commands-example.html

https://docs.aws.amazon.com/vpc/latest/userguide/vpc-subnets-commands-example-ipv6.html

https://docs.aws.amazon.com/vpc/index.html
