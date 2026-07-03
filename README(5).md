<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Launching VPC Resources

**Project Link:** [View Project](http://nextwork.ai/projects/aws-networks-ec2)

**Author:** volfsniper@gmail.com  
**Email:** volfsniper@gmail.com

---

## Launching VPC Resources

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-ec2_8ee57662)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is Virtual Private Cloud and it is useful because it provides privacy to our network and its resources.

### How I used Amazon VPC in this project

I used Amazon VPC to learn about VPC resource map.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was reviewing infrstructure of VPC but through this project I can now understand it.

### This project took me...

This project took me an hour.

---

## Setting Up Direct VM Access

Directly accessing a virtual machine means logging into and managing the operating system or software of the machine as if you were using it in front of you, but over the internet.

### SSH is a key method for directly accessing a VM

SSH, or Secure Shell, is the protocol we use for this secure access to a remote machine. When you connect to the instance, SSH verifies you possess the correct private key corresponding to the public key on the server, ensuring only authorized users can access the instance.

### To enable direct access, I set up key pairs

Key pairs help engineers directly access their virtual machines, like EC2 instances.

A private key's file format means cryptographic secret key which stored in client computer. My private key's file format was .PEM

---

## Launching a public server

Start your response with 'I had to change my EC2 instance's networking settings by selecting my VPC, after I select my subnet and security group.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-ec2_88727bef)

---

## Launching a private server

My private server has its own dedicated security group because we want to restrict its access to public internet.

My private server's security group's source is Public SG which means only instance which part of that group can access my private EC2 instance server.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-ec2_4a9e8014)

---

## Speeding up VPC creation

I used an alternative way to set up an Amazon VPC! This time, I chose VPC and more.

A VPC resource map is you can quickly understand the architectural layout of a VPC, like the number of subnets, which subnets are associated with which route table, and which route tables have routes to an internet gateway.

My new VPC has a CIDR block of /16. It is possible for my new VPC to have the same IPv4 CIDR block as my existing VPC because AWS VPCs are isolated from each other by default, so there won't be any IP conflicts unless we connect them using VPC peering

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-ec2_1cbb1b88)

---

## Speeding up VPC creation

### Tips for using the VPC resource map

When determining the number of public subnets in my VPC, I only had two options: 0 or 2. This was because  your public resources stay up even if one of the two Availaiblity Zones goes down.

The set up page also offered to create NAT gateways, which are None, Regional and Zonal. NAT gateway allows private resources to access the internet from any availability zone within a VPC, providing a single managed internet exit point for the entire region.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-ec2_8ee57662)

---

---
