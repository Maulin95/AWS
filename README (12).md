<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Fetch Data with AWS Lambda

**Project Link:** [View Project](http://nextwork.ai/projects/aws-compute-lambda)

**Author:** volfsniper@gmail.com  
**Email:** volfsniper@gmail.com

---

## Fetch Data with AWS Lambda

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-compute-lambda_p9thryj2)

---

## Introducing Today's Project!

In this project, I will demonstrate to create a DynamoDB databse. I'm doing this project to learn about DynamoDB.

### Tools and concepts

Services I used were DynamoDB, IAM, Lamda. Key concepts I learnt include Lambda functions, its permission to dynamoDB.

### Project reflection

This project took me approximately couple hours. The most challenging part was to create the role whle creating lambda function.

I chose to do this project today because I want to learn about fetching data from DynamoDB database through lamda function.

---

## Project Setup

To set up my project, I created a database using DynamoDB serivce. The partition key is userID. which means that from userID information my data will be stored in database.

In my DynamoDB table, I added user data. DynamoDB is schemaless, which means meaning you can add attributes as you need, and every item in your database can have a different set of attributes.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-compute-lambda_a112c3d5)

### AWS Lambda

AWS Lambda is a piece of code. I'm using Lambda in this project to run query, process data, respond to  events, and to run automated tasks.

---

## AWS Lambda Function

My Lambda function has an execution role, which allows to retrive data from DynamoDb. By default, the role grants basic permission.

My Lambda function will takes a userId as input, grabs the corresponding data from the UserData table, and returns it to you.

The code uses AWS SDK, which is in  JavaScript. My code uses SDK to interact with DynamoDB.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-compute-lambda_a1b2c3d5)

---

## Function Testing

To test whether my Lambda function works, I selected test Tab. The test is written in JSON code. If the test is successful, I'd see message as Executing function: succeeded

The test displayed a 'success' because the execution of the function but the function's response was actually in error because of the explicite permission is missing to access DynamoDB database.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-compute-lambda_u1v2w3x4)

---

## Function Permissions

To resolve the AccessDenied error, we have to give lambda function a permission to GetItem in other words we can add a permission policy that is missing.

There were four DynamoDB permission policies I could choose from, but I didn't pick them because none of them had GetItem action.

AmazonDynamoDBReadOnlyAccess was the right choice because it has GetItem action

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-compute-lambda_3ethryj2)

---

## Final Testing and Reflection

To validate my new permission settings, I ran the code to access UserData table and its records. The results were showing all the information because lamda function has permission to read data from database.

Web apps are a popular use case of using Lambda and DynamoDB. For example, I could use lambda function for news site to fetch news sites or blogs based on user queries.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-compute-lambda_p9thryj2)

---

## Enahancing Security

---

---
