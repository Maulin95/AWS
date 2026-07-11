<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# VPC Monitoring with Flow Logs

**Project Link:** [View Project](http://nextwork.ai/projects/aws-networks-monitoring)

**Author:** volfsniper@gmail.com  
**Email:** volfsniper@gmail.com

---

## VPC Monitoring with Flow Logs

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-monitoring_3e1e79a1)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is a Virtual private Cloud  and it is useful because it help your network by providing privacy.

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to cretae 2 networks and learn about analyzing the logs

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was learning about filtering the logs

### This project took me...

This project took me two hours to compelete.

---

## In the first part of my project...

### Step 1 - Set up VPCs

In this step, I will create 2 different VPCs.

### Step 2 - Launch EC2 instances

In this step, I will launch 2 EC2 instace because we need to monitor traffic and peer connection.

### Step 3 - Set up Logs

In this step, I will create a way to track all inbound and outbound traffic and  I will setup a place to store this traffic.

### Step 4 - Set IAM permissions for Logs

In this step, I will cretae an IAM roles for Flowlog because it needs a permission to write logs and send it to CloudWatch.

---

## Multi-VPC Architecture

I started my project by launching VPC. I have created 2 subnets.

The CIDR blocks for VPCs 1 and 2 are 10.1.0.0/16 and 10.2.0.0/16 respectively. They have to be unique because if they align then it may create some routing or connectivity issues.

### I also launched EC2 instances in each subnet

My EC2 instances' security groups allow all ICMP (ping) packets/traffic from another EC2 instance. This is because the security groups inbound rule.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-monitoring_e7fa8775)

---

## Logs

Logs are record, everything that happens, from users logging in to errors popping up. 

Log groups are a big folder in AWS where you keep related logs together. This log groups are region based but you can combine them.

### I also set up a flow log for VPC 1

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-monitoring_e8398869)

---

## IAM Policy and Roles

I created an IAM policy because VPC Flow Logs by default don't have the permission to record logs and store them in your CloudWatch log group. This policy makes sure that your VPC can now send log data to your log group

I also created an IAM role because VPC Flow logs need role not the policy

A custom trust policy is points to VPC Flow Logs as the only service that can use this role

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-monitoring_4334d777)

---

## In the second part of my project...

### Step 5 - Ping testing and troubleshooting

In this step, I will send an ICMP packets from first instance to another so that we logs can be traced.

### Step 6 - Set up a peering connection

In this step, I will create a VPC peering which makes connection between two VPC.

### Step 7 - Analyze flow logs

In this step, I will review the flow logs.

---

## Connectivity troubleshooting

My first ping test between my EC2 instances had no replies, which means I have no connection over private IP to other EC2 instance.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-monitoring_99d4ba42)

I could receive ping replies if I ran the ping test using the other instance's public IP address, which means my EC2 instance is connected to IGW and I can reach over public IP.

---

## Connectivity troubleshooting

Looking at VPC 1's route table, I identified that the ping test with Instance 2's private address failed because it is missing route from peer connection

### To solve this, I set up a peering connection between my VPCs

I also updated both VPCs' route tables so that ICMP packets can be reached to destination EC2 or another VPC.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-monitoring_7316a13d)

---

## Connectivity troubleshooting

I received ping replies from Instance 2's private IP address! This means the ICMP packets can be now reached through peering connection.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-monitoring_4ec7821f)

---

## Analyzing flow logs

Flow logs tell us about the size of the data packets, source the data came from, port that is used and other information.

For example, the flow log I've captured tells us ping messages failed to reach instance 2.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-monitoring_d116818e)

---

## Logs Insights

Logs Insights is a CloudWatch feature that analyzes your logs. In Log Insights, you use queries to filter, process and combine data to help you troubleshoot problems or better understand your network traffic!

I ran the query 
stats sum(bytes) as bytesTransferred by srcAddr, dstAddr
| sort bytesTransferred desc
| limit 10

This query analyzes the transferred bytes/data between source and destination with limit of 10.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-monitoring_3e1e79a1)

---

---
