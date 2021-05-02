---
title: "Lab1 - Stand-up GitLab Ultimate"
chapter: true
weight: 3
---

In This lab we will spin-up GitLab Ultimate AMI in AWS.


- Open [GitLab Ultimate](https://aws.amazon.com/marketplace/pp/B07SJ817DX) in AWS Marketplace.
- Click on **Continue to Subscribe**
- Sign in with your IAM user
- Click on Continue to Configuration
- Leave the default value for **Delivery Method**, Select the latest version in **Software Version**, Select your **Region**, click **Continue to Launch**.

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
