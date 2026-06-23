<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Host a Website on Amazon S3

**Project Link:** [View Project](http://nextwork.ai/projects/aws-host-a-website-on-s3)

**Author:** volfsniper@gmail.com  
**Email:** volfsniper@gmail.com

---

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Introducing Today's Project!

### Project overview

In this project, I will demonstrate... I'm doing this project to demonstrate how I can deploy static website using S3 bucket in AWS

### Tools and concepts

Services I used were Amazon S3 Key concepts I learnt include Storage, ACL.

### Time, challenges, and wins

This project took me approximately 20 minutes. The most challenging part was figuring out ACL permission. It was most rewarding too.

---

## How I Set Up an S3 Bucket

### What I did in this step

In this step, I will creating a storage space for my website objects.

### How long it took to create the bucket

Creating an S3 bucket took me few minutes.

### Region selection

The Region I picked for my S3 bucket was North Verginia because due to low latency and same region.

### Understanding bucket name uniqueness

S3 bucket names are globally unique! This means that it can be easily identified and content can't be access by unknown people.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-host-a-website-on-s3_ba6d42ad)

---

## Upload Website Files to S3

### What I did in this step

In this step, I will download both website content files and then upload it to S3 bucket.

### Files I uploaded

I uploaded two files to my S3 bucket - they were index.html and one folder name NextWork - Everyone should be in a job they love_files/

### How the files work together

Both files are necessary for this project as one carry the index file like an HTML code congifuration another folder carries all the pictures, JavaScript, and other files.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-host-a-website-on-s3_a265af88)

---

## Static Website Hosting on S3

### What I did in this step

In this step, I will make website public.

### Understanding website hosting

Website hosting means, it is accessible by public

### How I enabled website hosting

To enable website hosting with my S3 bucket, I select S3 static website hosting Enable.

### Access Control Lists (ACLs)

An ACL is a set of rules that controls the access of your data, you can enable it or keep it disable. I did Enable it for this project.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-host-a-website-on-s3_c22c54c0)

---

## Bucket Endpoints

### Understanding bucket endpoint URLs

Once static website is enabled, S3 produces a bucket endpoint URL, which is http://sounds-collection-m.s3-website-us-east-1.amazonaws.com

### What I saw when I tested the endpoint

When I first visited the bucket endpoint URL, I saw a web page with error message. The reason for this error was Objects permission.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-host-a-website-on-s3_22ce4daf)

---

## Success!

### What I did in this step

In this step, I will change the objects permissions to make it public.

### How I resolved the 403 error

To resolve this 403 Forbidden error, I selected each object and click on Action and select option "Make Public using ACL"

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Bucket Policies

### What I did in this extension

### Understanding bucket policies

### What my bucket policy does

---

---
