---
title: "Lab1 - Stand-up GitLab Ultimate"
chapter: true
weight: 3
---

In This lab we will spin-up GitLab Ultimate AMI in AWS.


- Open [GitLab Ultimate](https://aws.amazon.com/marketplace/pp/B07SJ817DX) in AWS Marketplace.
- Click on **Continue to Subscribe**
- Sign in with your IAM user.
- Click on **Continue to Configuration**.
- Leave the default value for **Delivery Method**, Select the latest version in **Software Version**, Select your **Region**, click **Continue to Launch**.
- In Lunch this software page, scroll down, under **Security Group Settings** click **Create New Based On Seller Settings** .
- Name your security group, add a description, and Save it.
- Select **Key Pair**. If you don't have key pair, create one.
- Leave other fields in this page with default values.  Click **Launch**.
- You will get Congratulations message confirming you launched the machine successfully.
- In this message click on **EC2 Console** link.
- Click on your instance ID link.
- Click Open address.
- It takes a few minutes to start the server, you may see this error, this is ok, wait 1 minute and refresh the page.
- You are now should be able to access GitLab login page. username is **root**, password is your **instance ID**, click **Sign in**.
- Congratulations! you managed to start GitLab instance and sign in to it.

- run untagged jobs
-
1. container setup
curl -fsSL https://get.docker.com -o get-docker.sh
 sudo sh get-docker.sh

 {{% notice tip %}} When creating additional sections or pages, copy the files and folders from another section, rename and edit.
 {{% /notice %}}

 {{% notice note %}} To make the creation of web page documentation easier, we utilize a tool called Hugo. You will write your documentation/instructions using markdown language and Hugo will create static html content that can be served via S3. Hugo additionally applies a theme so that the site will have an AWS look and feel plus add additional features to beautify and make content stand out.

 For more information about installing and using Hugo, visit https://gohugo.io/getting-started/installing/

 For more information about the learn theme used in Hugo, visit https://learn.netlify.com/en/ {{% /notice %}}
