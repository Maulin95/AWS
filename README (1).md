<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Cloud Security with AWS IAM

**Project Link:** [View Project](http://nextwork.ai/projects/aws-security-iam)

**Author:** volfsniper@gmail.com  
**Email:** volfsniper@gmail.com

---

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-security-iam_1c864649)

---

## Introducing Today's Project!

### Project overview

In this project, I will demonstrate IAM Services. I'm doing this project to learn  IAM Policy creation and IAM Users and Groups understanding.

### Tools and concepts

Services I used were EC2, IAM User, Groups, and Policy. Key concepts I learnt include launching EC2 instances, creating custome IAM Policies, Apply this policies to groups and add users to the groups.

### Project reflection

This project took me approximately 15 minutes. The project went smooth with all the provided steps.

---

## Tags

### What I did in this step

In this step, I will Launch 2 EC2 instances

### Understanding tags

Tags are identifiers, This tagging helps us with identifying all resources with the same tag at once.

### My tag configuration

The tag I’ve used on my EC2 instances is called Env The value I’ve assigned for my instances are network-dev-myName

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-security-iam_2e0e5a5d)

---

## IAM Policies

### What I did in this step

In this step, I will create IAM policies so that user can do their daily assigned tasks.

### Understanding IAM policies

IAM Policies are set of rules that allows user or groups to do certain tasks.

### The policy I set up

For this project, I’ve set up a policy using JSON.

### Policy effect

I’ve created a policy that effect allow and deny user actions on appropriate EC2 instance.

### Understanding Effect, Action, and Resource

The Effect, Action, and Resource attributes of a JSON policy means that certain operations can be conduct by certain users only otherwise it will give you error.

---

## My JSON Policy

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-security-iam_1c864649)

---

## Account Alias

### What I did in this step

In this step, I will create account alias so I can have account URL with alias name instead of account ID

### Understanding account aliases

An account alias is an Account Alias is a friendly name for your AWS account that you can use instead of your account ID (which is usually a bunch of digits) to sign in to the AWS Management Console.

### Setting up my account alias

Creating an account alias took me few seconds.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-security-iam_0eb4439b)

---

## IAM Users and User Groups

### What I did in this step

In this step, I will create IAM group and Users because IAM permission will be assign and User will be part of this Groups.

### Understanding user groups

IAM user groups are user groups are the collections/folders of users for easier user management.

### Attaching policies to user groups

I attached the policy I created to this user group, which means I don't need to assign same permission to all users which is part of this group.

### Understanding IAM users

IAM users are IAM users are the people that will get access to your resources/AWS account

---

## Logging in as an IAM User

### Sharing sign-in details

The first way is Email sign in instruction or download the .csv file and share it.

### Observations from the IAM user dashboard

Once I logged in as my IAM user, I noticed several of the services not availble. This was because of the policy.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-security-iam_6f2ab446)

---

## Testing IAM Policies

### What I did in this step

In this step, I will test user login 

### Testing policy actions

I tested my JSON IAM policy by login to user and try to stop the instance

### Stopping the production instance

When I tried to stop the production instance it gets an error. This was because of the policy

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-security-iam_0e7a9d6a)

### Stopping the development instance

Next, when I tried to stop the development instance it sops.  This was because of the policy

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-security-iam_1811801c)

---

## IAM Policy Simulator

To extend my project, I'm going to use IAM Tools name Policy Simulator.

### Understanding the IAM Policy Simulator

The IAM Policy Simulator is a tool which can help to run a real time environment like situation It's useful for performing task such as delete, stop EC2 instances.

### How I used the simulator

I set up a simulation for Delete Tags and Stop Inances The results were I had to adjust the tags to specific.

![Image](http://nextwork.ai/positive_red_glamorous_feijoa/uploads/aws-security-iam_069d8a621)

---

---
