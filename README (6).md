<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Testing VPC Connectivity

**Project Link:** [View Project](http://nextwork.ai/projects/aws-networks-connectivity)

**Author:** volfsniper@gmail.com  
**Email:** volfsniper@gmail.com

---

## Testing VPC Connectivity

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-connectivity_8ee57662)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is Virtual Private Cloud and it is useful because it can help provide privacy to your resources.

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to check connectivity of public server to internal private server and internet.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was to learn that I can connect internet and private server both through one instance at the same time.

### This project took me...

This project took me couple of hours.

---

## Connecting to an EC2 Instance

Connectivity means how well your instances are connecting each other within the network and outside of the network.

My first connectivity test was whether I could connect to my public web server

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-connectivity_88727bef)

---

## EC2 Instance Connect

I connected to my EC2 instance using EC2 Instance Connect, which is command line interface.

My first attempt at getting direct access to my public server resulted in an error, because in my security group inbound rules I had HTTP request allowd but not the SSH.

I fixed this error by adding a inbound rule of SSH from anywhere.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-connectivity_1cbb1b88)

---

## Connectivity Between Servers

Ping is a tool which uses ICMP protocol of TCP. I used ping to test the connectivity between my public web server to private webserver.

The ping command I ran was ping 10.0.1.X

The first ping returned just one line.This meant it tries to connect private EC2 instance. 

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-connectivity_defghijk)

---

## Troubleshooting Connectivity

I troubleshooted this by going through private subnet routing, ACL routes and Security group settings.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-connectivity_4a9e8014)

---

## Connectivity to the Internet

Curl is curl is a tool to test connectivity in a network.

I used curl to test the connectivity between public AWS to internet

### Ping vs Curl

curl is used to transfer data to or from a server. That means on top of checking connectivity, you can use curl to grab data from, or upload data into other servers on the internet! Where ping checks if one computer can contact another

---

## Connectivity to the Internet

I ran the curl command curl https://nextwork.ai/projects/aws-host-a-website-on-s3 which returned combination of HTML, Java script code.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-connectivity_8ee57662)

---

---
