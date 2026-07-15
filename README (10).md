<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# VPC Endpoints

**Project Link:** [View Project](http://nextwork.ai/projects/aws-networks-endpoints)

**Author:** volfsniper@gmail.com  
**Email:** volfsniper@gmail.com

---

## VPC Endpoints

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-endpoints_09bcaa8a)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is Vritual private cloud and it is useful because it help you maintaining awss reources privacy.

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to connect S3 bucket over VPC endpoint

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was to learn about bucket policy.

### This project took me...

This project took me an hour.

---

## In the first part of my project...

### Step 1 - Architecture set up

In this step, I will create VPC resources, EC2 instace and S3 bucket.

### Step 2 - Connect to EC2 instance

In this step, I will connect EC2 instace to internet.

### Step 3 - Set up access keys

In this step, I will configure aws envirnment because to access s3 bucket, EC2 instace need AWS environment.

### Step 4 - Interact with S3 bucket

In this step, I will connect my S3 bucket to Ec2 instance via public access.

---

## Architecture set up

I started my project by launching VPC and its resources following by launching an EC2 instace.

I set up S3 bucket and upload images/files.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-endpoints_4334d777)

---

## Access keys

### Credentials

To set up my EC2 instance to interact with my AWS environment, I configured AWS access key, Secret key, region where S3 bucket is and output format.

Access keys are part of our credrntials which is made of username and password.

Secret access keys are like the password that pairs with your access key ID (your username). You need both to access AWS services.

### Best practice

Although I'm using access keys in this project, a best practice alternative is to use IAM role and policies to this role then attach this role to EC2 instance.

---

## Connecting to my S3 bucket

The command I ran was aws s3 ls. This command is used to list the S3 buckets in your account.

The terminal responded with the S3 bucket list. This indicated that the access keys I set up was success.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-endpoints_4334d778)

---

## Connecting to my S3 bucket

I also tested the command aws s3 ls s3://nextwork01-vpc-maulin which returned the list of files in the bucket.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-endpoints_4334d779)

---

## Uploading objects to S3

To upload a new file to my bucket, I first ran the command touch to create an empty file.

The second command I ran was cp. This command will copy the file from EC2 instace to S3 storage.

The third command I ran was aws s3 ls s3://nextwork-vpc-maulin. which validated that file is copied to S3 sotrage

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-endpoints_3e1e79a2)

---

## In the second part of my project...

### Step 5 - Set up a Gateway

In this step, I will setup a VPC endpoint because that way I can connect S3 directly rather than through internet.

### Step 6 - Bucket policies

we are about to restrict the access of S3 bucket. Only traffic comming through my endpoint can access this bucket. 

### Step 7 - Update route tables

In this step, I will try to access the S3 bucket again to see if connection go through VPC endpoint.

### Step 8 - Validate endpoint conection

In this step, I will test the connection to my S3 bucket through EC2 instance.

---

## Setting up a Gateway

I set up an S3 Gateway, which is an endpoint used specifically for Amazon S3 and DynamoDB

### What are endpoints?

An endpoint in AWS is a service that allows private connections between your VPC and other AWS services without needing the traffic to go over the internet.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-endpoints_09bcaa8a)

---

## Bucket policies

A bucket policy is a type of IAM policy designed for setting access permissions to an S3 bucket. Using bucket policies, you get to decide who can access the bucket and what actions they can perform with it.

My bucket policy will deny all the traffic coming through internet and only allow traffic coming from VPC endpoint.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-endpoints_7316a13d)

---

## Bucket policies

Right after saving my bucket policy, my S3 bucket page showed 'denied access' warnings. This was because I've blocked access through the policy.

I also had to update my route table because updating route table open the connection to VPC endpoint and I can get access to S3 bucket.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-endpoints_4ec7821f)

---

## Route table updates

To update my route table, I go endpoint and select the Route table tab and then click on manage route table. After that I have select correct subnet which makes the route.

After updating my public subnet's route table, my terminal could return to have an access of my S3 bucket and its files.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-endpoints_d116818e)

---

## Endpoint policies

An endpoint policy is a way to detemine the access of your aws resources.

I updated my endpoint's policy by deny the access. I could see the effect of this right away, because I can't access my S3 bucket files.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-endpoints_3e1e79a3)

---

---
