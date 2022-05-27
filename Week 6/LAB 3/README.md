# Working with AWS DynamoDB

Task:
1. Create a Table
2. Write Data to a Table Using the Console or AWS CLI
3. Read Data from a Table
4. Update Data in a Table
5. Query Data in a Table
Items returned (3)

1



Users
InvoiceID
Date
Users
InvoiceID
Date
Segun Tomori	ID0002	May 25, 2022
Onigbinde Seye	ID0001	May 26, 2021
Tuniola Feranmi	ID0003	May 27, 2022

6. Create a Global Secondary Index

Global secondary indexes (1)Info
Delete
Create index

1


Find indexes
Name
Status
Partition key
Sort key
Read capacity
Write capacity
Projected attributes
Size
Item count

Date-index	
 Active
Date (String)	-	
Range: 1 - 10
Auto scaling at 70%
Current provisioned units: 1
Range: 1 - 10
Auto scaling at 70%

Current provisioned units: 1
All	0 bytes	0



7. Query the Global Secondary Index
8. Clean Up actions


Guide:
https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/GettingStartedDynamoDB.html