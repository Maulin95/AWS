<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Access S3 from a VPC

**Project Link:** [View Project](http://nextwork.ai/projects/aws-networks-s3)

**Author:** volfsniper@gmail.com  
**Email:** volfsniper@gmail.com

---

## Access S3 from a VPC

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-s3_3e1e79a2)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is vitual private cloud and it is useful because it can provide privacy to your EC2 instance.

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to create its resource and then connect EC2 instace to S3 storage.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was learning how to acces S3 through command line

### This project took me...

This project took me few hours.

---

## In the first part of my project...

### Step 1 - Architecture set up

In this step, I will create VPC and other resources to connect with S3 storage.

### Step 2 - Connect to my EC2 instance

In this step, I will connect EC2 instance to public internet.

### Step 3 - Set up access keys

In this step, I will create an access Key and give acces to AWS environment to my EC2 instance.

---

## Architecture set up

I started my project by launching virtual private cloud following by Subnet, IGW, ACL, Security Group and EC2 instances.

I did set up S3 bucket and upload files in the bucket.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-s3_4334d777)

---

## Running CLI commands

AWS CLI is Command line Interface. I have access to AWS CLI because in my security group I have allowed traffic for SSH.

The first command I ran was aws s3 ls. This command is used to list the S3 buckets in your account

The second command I ran was aws configure. This command is used to configure and access S3 bucket list.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-s3_e7fa8776)

---

## Access keys

### Credentials

To set up my EC2 instance to interact with my AWS environment, I configured S3 bucket.

Access keys are credentials made up of  a usename and password.

The secret access key is like the password that pairs with your access key ID (your username). You need both to access AWS services

### Best practice

Although I'm using access keys in this project, a best practice alternative is to use IAM role with appropriate policies.

---

## In the second part of my project...

### Step 4 - Set up an S3 bucket

In this step, I will create S3 bucket.

### Step 5 - Connecting to my S3 bucket

In this step, I will connect my EC2 instace to connect with S3 bucket.

---

## Connecting to my S3 bucket

The first command I ran was aws s3 ls. This command is used to list the S3 buckets in your account

When I ran the command aws s3 ls again, the terminal responded withlist of S3 bucket names This indicated that my EC2 instance is now connected with s3 bucket.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-s3_4334d778)

---

## Connecting to my S3 bucket

Another CLI command I ran was aws s3 ls s3://nextwork-vpc-project-maulin. which returned me the list of files in my bucket.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-s3_4334d779)

---

## Uploading objects to S3

To upload a new file to my bucket, I first ran the command sudo touch /tmp/test.txt. This command creates an empty text file.

The second command I ran was aws s3 cp /tmp/test.txt s3://nextwork-vpc-project-maulin. This command will copy the file to my S3 bucket.

The third command I ran was aws s3 ls s3://nextwork-vpc-project-maulin. which validated that my file is present in S3 bucket.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-s3_3e1e79a2)

---

---
