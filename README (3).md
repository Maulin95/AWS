<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# VPC Traffic Flow and Security

**Project Link:** [View Project](http://nextwork.ai/projects/aws-networks-security)

**Author:** volfsniper@gmail.com  
**Email:** volfsniper@gmail.com

---

## VPC Traffic Flow and Security

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-security_92b0b0b4)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is virtual private cloud that provides privacy to all your resources and it is useful because we can control the traffic flows that allowed/deny in the network

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to create and learn about subnets, Network ACLs, Security Group and other services.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was learning about rules and data packets.

### This project took me...

This project took me half hour.

---

## Route tables

Route tables are paths which your data took to reach to the destination from source. Where destination can be your resources and source will be the Internet or another node.

Routes tables are needed to make a subnet public because When a subnet's route table has a route that directs internet-bound traffic to the internet gateway, the subnet becomes a public subnet. This means your subnet can communicate with the internet.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-security_0a07b191)

---

## Route destination and target

Routes are defined by their destination and target, which mean those targets has permission to allow/deny traffic from source.

The route in my route table that directed internet-bound traffic to my internet gateway had a destination of 0.0.0.0/0 and a target of my IGW.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-security_0a07b191)

---

## Security groups

Security groups are collection of the rules for traffic that comes in and goes out of the network.

### Inbound vs Outbound rules

Inbound rules are tracing traffic comming into the network. I configured an inbound rule that allows HTTP request.

Outbound rules are the traffic that goes out of your network basically a response of your request. By default, my security group's outbound rule has All traffic allowd.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-security_92b0b0b4)

---

## Network ACLs

Network ACLs are traffic cops stationed at every entry and exit point of your subnet, checking each data packet against a table of ACL rules before allowing them through

### Security groups vs. network ACLs

The difference between a security group and a network ACL is that Network ACLs are used to set broad traffic rules that apply to an entire subnet and security group rules are applies to group of resources or individual resource.

---

## Default vs Custom Network ACLs

### Similar to security groups, network ACLs use inbound and outbound rules

By default, a network ACL's inbound and outbound rules will allow all inbound and outbound traffic.

In contrast, a custom ACL’s inbound and outbound rules are automatically set to deny all the traffic.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-security_4faeb056)

---

## Tracking VPC Resources

---

---
