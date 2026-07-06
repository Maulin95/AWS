<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# VPC Peering

**Project Link:** [View Project](http://nextwork.ai/projects/aws-networks-peering)

**Author:** volfsniper@gmail.com  
**Email:** volfsniper@gmail.com

---

## VPC Peering

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-peering_88727bef)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is Virtual Private Cloud and it is useful to maintain privacy of your AWS resources.

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to learn about VPC Peering in different public networks.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was to learn about Elastic IP.

### This project took me...

This project took me two hours.

---

## In the first part of my project...

### Step 1 - Set up my VPC

In this step, I will create Two VPCs from scratch using VPC resources.

### Step 2 - Create a Peering Connection

In this step, I will create a link betweem two VPC.

### Step 3 - Update Route Tables

In this step, I will make routes because it will be decideing waether traffic to allow or deny comming from VPC 1 or VPC 2.

### Step 4 - Launch EC2 Instances

In this step, I will create and launch an EC2 instances in each VPCs to test connection of VPC peering.

---

## Multi-VPC Architecture

I started my project by launchingVPC resource map by selecting VPC and more. In total I have created 2 public subnets.

The CIDR blocks for VPCs 1 and 2 are 10.1.0.0/16 and 10.2.0.0/16 respectively. They have to be unique because resources in wach network has different access rights.

### I also launched 2 EC2 instances

I didn't set up key pairs for these EC2 instances as part of this project so we can directly access the instance.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-peering_11111111)

---

## VPC Peering

A peering connection lets VPCs and their resources route traffic between them using their private IP addresses. This means data can now be transferred between VPCs without going through the public internet.

VPCs would use peering connections to data transfers between VPCs would use resources' public address - meaning VPCs have to communicate over the public internet.

The difference between a Requester and an Accepter in a peering connection is requestor can request connection to another VPC but it is really dependent on Accepter to whether to accept or deny the request.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-peering_1cbb1b88)

---

## Updating route tables

After accepting a peering connection, my VPCs' route tables need to be updated because with out adding peering route there will be no link to communicate between two VPC.

My VPCs' new routes have a destination of each VPCs CIDE block which is 10.1.0.0/16 and 10.2.0.0/16. 

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-peering_4a9e8014)

---

## In the second part of my project...

### Step 5 - Use EC2 Instance Connect

In this step, I will try to connect my EC2 instance

### Step 6 - Connect to EC2 Instance 1

In this step, I will try to connect EC2 instance after fixing error related to public IPV4

### Step 7 - Test VPC Peering

In this step, I will test the connectivity between instance 1 and Instance 2

---

## Troubleshooting Instance Connect

Next, I used EC2 Instance Connect to Elastic IP.

I was stopped from using EC2 Instance Connect as I haven't assign public IP address to it.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-peering_7685490c)

---

## Elastic IP addresses

To resolve this error, I set up Elastic IP addresses. Elastic IPs are static IPv4 addresses that get allocated to your AWS account, and is yours to delegate to an EC2 instance.

Associating an Elastic IP address resolved the error because I assign this dedicated Ip to respective instance.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-peering_45663498)

---

## Troubleshooting ping issues

To test VPC peering, I ran the command ping X.X.X.X (2nd EC2 IP).

A successful ping test would validate my VPC peering connection because each response has different sequence number and shows response in new line.

I had to update my second EC2 instance's security group because it was missing ICMP permission I added a new rule that ICMP request from another VCP is allowed

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-peering_7a29d352)

---

---
