
# Amazon Lambda

- Lambda is a compute service that lets you run code without managing servers
- Lambda executes your code when needed
- It scales automatically from a few request per second to thousand per second
- It works on pay as you go model
  means you only pay for compute time you consumed. No charges when code is not running
- Lambda supports NodeJS, Java, Python, Ruby, C#, Go, .net, powershell
---
### Lambda manages:

1. Provisioning and capacity of the compute fleets
   (CPU, Network and other issues)
2. Server and OS maintenance
3. High availability and autoscaling
4. Monitoring health
5. Deploying a code
6. Monitoring lambda function


---
##  EC2 vs Lambda Comparison

| Feature           | EC2                                                     | Lambda                         |
| ----------------- | ------------------------------------------------------- | ------------------------------ |
| Service Type      | IaaS service                                            | PaaS service                   |
| Nature            | Virtual machine as server                               | It is serverless function      |
| Execution Time    | Unlimited execution time is there                       | Maximum 15 minutes to execute  |
| Usage             | Used for full application                               | Used for event-based tasks     |
| State Management  | Stateful                                                | Stateless                      |
| Server Management | Requires server management - server management required | Server management not required |


---

##  How Lambda Works?
1. You upload your code to AWS Lambda.
2. Lambda runs the code when triggered (event-based).
3. AWS automatically provisions and manages the required servers.
4. It scales automatically based on the number of requests.
5. After execution, resources are released automatically.

---

![image alt](https://github.com/Ashu-1808/AWS-cloud-computing-for-devops/blob/4498e13f3283fcf18026dfb4c60dfee9cf33f2e2/Lambda%20.png)
---
##  Lambda Function
1. The code you upload to AWS Lambda is called a **Lambda Function**.
2. It runs only when triggered by an event.
3. Example triggers: S3 upload, API Gateway request, DynamoDB change, etc.

---

##  Pricing
1. You are charged based on:
  a. Number of requests
  b. Duration (execution time in milliseconds)
2. Pay-as-you-go model
3. No charge when function is not running

---

##  Drawbacks

1. Minimum execution time: ~3 seconds
2. Maximum execution time: 900 seconds (15 minutes)
3. Not suitable for long-running applications

---

## Lambda + DynamoDB Integration Step-by-Step :
```
1. Create S3 Bucket
 - Create an S3 bucket
 - (It should be in the same region as Lambda)

2. Create Lambda Function
 - Go to Lambda → Create Function
 - Choose runtime (e.g., Python 3.x)
 - Use supported version of language
 - Create the function

3. Add Code
 - Add the code you have written
 - Code should insert data into DynamoDB

4. Create DynamoDB Table
 - Go to DynamoDB
 - Create Table (New table)
 - Add Table name (as mentioned in code)
 - Create Partition key (as used in code)

5. Add Trigger
 - Go to Lambda → My Function
 - Add Trigger
 - Select S3
 - Choose the bucket you created earlier

6. Configure Permissions
 - Go to Configuration → Permissions
 - Select default role name
 - Attach policy
 - Add permissions:
   a. AmazonDynamoDBFullAccess
   b. AmazonS3FullAccess

7. Test the Setup
 - Enter S3 bucket
 - Upload an item/file to S3 bucket
 - Go to DynamoDB
 - Check if data is added in the table

8. Cleanup (Optional)
 - Delete S3 Bucket
 - Delete DynamoDB Table
 - Delete Lambda Function
```




