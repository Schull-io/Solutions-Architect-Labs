# Working with placement Groups using AWS CLI

Tasks:
1. Create a placement group
{
    "PlacementGroup": {
        "GroupName": "seye-cluster",
        "State": "available",
        "Strategy": "cluster",
        "GroupId": "pg-0ec3c59b9345913d9",
        "Tags": [
            {
                "Key": "purpose",
                "Value": "production"
            }
        ],
        "GroupArn": "arn:aws:ec2:us-east-1:403531065616:placement-group/seye-cluster"
    }
}

2. Tag a placement group
{
    "Tags": [
        {
            "Key": "SeyeTags",
            "ResourceId": "pg-058581bca94ed6edb",
            "ResourceType": "placement-group",
            "Value": ""
        },
        {
            "Key": "purpose",
            "ResourceId": "pg-0ec3c59b9345913d9",
            "ResourceType": "placement-group",
            "Value": "production"
        }
    ]
}
3. Launch instances in a placement group
4. Describe instances in a placement group
5. Change the placement group for an instance
6. Delete a placement group


Guide:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html#using-placement-groups
