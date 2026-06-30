<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Creating a Private Subnet

**Project Link:** [View Project](http://nextwork.ai/projects/aws-networks-private)

**Author:** volfsniper@gmail.com  
**Email:** volfsniper@gmail.com

---

## Creating a Private Subnet

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-private_afe1fdbd)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is Virtual Private Cloud. It is useful because it can provide public and private subnet through which we can protect important data while connecting to internet.

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to create private subnet, route table and private ACL.

### One thing I didn't expect in this project was...

None

### This project took me...

This project took me few minutes to finish this project

---

## Private vs Public Subnets

The difference between public and private subnets is that public subnet contains resources that communicate directly with the internet. A private subnet isolates sensitive resources from the internet

Having private subnets are useful because we can control access to EC2 instace expose to external network and then store confidential data.

My private and public subnets cannot have the same CIDR block

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-private_afe1fdbd)

---

## A dedicated route table

By default, my private subnet is associated with local.

I had to set up a new route table for private subnet resources because eventually it has to communicate with other internal resources.

My private subnet's dedicated route table only has one inbound and one outbound rule that allows local target.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-private_b4b904b5)

---

## A new network ACL

By default, my private subnet is associated with Private NACL

I set up a dedicated network ACL for my private subnet because I have to deny all the incoming and outgoing request from that subnet.

My new network ACL has two simple rules -Deny all incoming and outgoing traffic

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-private_1ed2cb07)

---

---
