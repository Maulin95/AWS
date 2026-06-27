<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Build a Virtual Private Cloud

**Project Link:** [View Project](http://nextwork.ai/projects/aws-networks-vpc)

**Author:** volfsniper@gmail.com  
**Email:** volfsniper@gmail.com

---

## Build a Virtual Private Cloud (VPC)

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-vpc_2facf927)

---

## Introducing Today's Project!

In this project, I will demonstrate on How to Cretae VPC, Subnet, and Internet Gateway in AWS.

### What is Amazon VPC?

Amazon VPC is virtual private cloud which allowa your resources a privacy. and it is useful because with out VPC resources would be randomly scattered with no privacy or personal space, so everyone could see and access everyone else's resources 

In today's project, I used Amazon VPC to create subnet and assign IGW.

### Personal reflection

This project took me few minutes

One thing I didn't expect in this project was showing how I can enable assigning public IP automatically after creating subnet.

---

## Virtual Private Clouds (VPCs)

### What I did in this step

In this step, I will access VPC in AWS console. Then I will click on cretae VPC option

### How VPCs work

VPCs are boundry of your resources. So your resources can't be access by others on internet. In nutshell, VPC will provide privacy.

### Why there is a default VPC in AWS accounts

There was already a default VPC in my account ever since my AWS account was created. This is to make sure I can access all AWS services even which require internet or VPC configuration.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-vpc_2facf927)

### Defining IPv4 CIDR blocks

To set up my VPC, I had to define an IPv4 CIDR block, which is a block size of my available IPV4 addresses that I can assign to my various resources.

---

## Subnets

### What I did in this step

In this step, I will create Subnet. because through this step I can difine range of IP address that are available for users.

### Creating and configuring subnets

Subnets are like different neighborhoods inside your city. You use subnets to group resources with similar access rules and restrictions. Some subnets might be public areas that all resources can access (public subnets) while others are private areas with limited access (private subnets)There are already subnets existing in my account, one for every availability zone.

### Public vs private subnets

The difference between public and private subnets are resources connection to internet. Recources connected to public subnet can access external network and public subnet resources communicate with the subnet. For a subnet to be considered public, it has to be connected to internet gateway.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-vpc_157c4219)

### Auto-assigning public IPv4 addresses

Once I created my subnet, I enabled auto-assign public IPV4. This setting makes sure EC2 instance launched in that subnet will instantly get a public IP address so you won't have to create one manually.

---

## Internet gateways

### What I did in this step

In this step, I will create Internet gateway to attach my VPC.

### Setting up internet gateways

An internet gateway connects your VPC to the outside world (internet).

Attaching an internet gateway to a VPC means attaching an internet gateway means resources in your VPC can now access the internet. If I missed this step, my application will not be availble to internet users or my resources may not able to access external resources.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-vpc_4ae90410)

---

## Using the AWS CLI

### What I'm doing in this extension

### Exploring CloudShell and CLI

### Debugging my setup

### Comparing CloudShell vs AWS Console

---

---
