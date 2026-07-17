<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Website Delivery with CloudFront

**Project Link:** [View Project](http://nextwork.ai/projects/aws-networks-cloudfront)

**Author:** volfsniper@gmail.com  
**Email:** volfsniper@gmail.com

---

## Website Delivery with CloudFront

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-cloudfront_1dddddwe)

---

## Introducing Today's Project!

In this project, I will demonstrate a website using S3 bucket and AWS CloudFront service. I'm doing this project to learn how to deploy a website with cloudFront.

### Tools and concepts

Services I used were CloudFront and S3. Key concepts I learnt include content delivery network (CDN), OAC, and S3 bucket policy.

### Project reflection

This project took me approximately an hour. The most challenging part was learning about the policies. It was most rewarding to see web page after it deploy the distribution.

I chose to do this project today because I need to learn about CloudFront service. Something that would make learning with NextWork even better is amazing hands on lab experience.

---

## Set Up S3 and Website Files

I started the project by creating an S3 bucket to store the files. I can't use CloudFront for this task because CloudFront only host the content.

The three files that make up my website are index.html, which is html frontend code. Style.css, which is a desuging code of the html webpage and script.js, which is a function/logic.

I validated that my website files work by clicking on Submit button.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-cloudfront_qgo7wcd3)

---

## Exploring Amazon CloudFront

Amazon CloudFront is a content delivery network, which means it speeds up the distribution of your static and dynamic web content. Businesses and developers use CloudFront because of the best possible performance.

To use Amazon CloudFront, you set up distributions, which are Single website or App and Multi-tent-architecture. I set up a distribution for Single website or App. The origin is S3.

My CloudFront distribution's default root object is Amazon S3 This means my  files will be stored in S3 bucket.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-cloudfront_qgo7wcdt)

---

## Handling Access Issues

When I tried visiting my distributed website, I ran into an access denied error because CloudFront has no permission to access our S3 bucket.

My distribution's origin access settings were Origin access control settings. This caused the access denied error because it gives the access to only cloudFront.

To resolve the error, I set up origin access control (OAC). OAC is a special user for CloudFront that prevents unwanted access.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-cloudfront_egrhntyu)

---

## Updating S3 Permissions

Once I set up my OAC, I still needed to update my bucket policy because OAC's role makes sure that CloudFront can access the files from S3 bucket but to make website publically available we need to update bucket policy.

Creating an OAC automatically gives me a policy I could copy, which grants permission to CloudFront to access the bucket.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-networks-cloudfront_eg98ntyu)

---

## S3 vs CloudFront for Hosting

---

## S3 vs CloudFront Load Times

---

---
